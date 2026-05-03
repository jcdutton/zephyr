# Copyright (c) 2023 Nordic Semiconductor ASA
# SPDX-License-Identifier: Apache-2.0

set(cmsis_glue_path ${ZEPHYR_CMSIS_MODULE_DIR})
add_subdirectory(${ZEPHYR_CURRENT_MODULE_DIR} cmsis)

if(CONFIG_CPU_CORTEX_M OR CONFIG_CPU_AARCH32_CORTEX_A OR CONFIG_CPU_AARCH32_CORTEX_R)
  zephyr_include_directories(.)
  zephyr_include_directories(${cmsis_glue_path}/CMSIS/Core/Include)
endif()
