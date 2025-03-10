#
# Copyright (c) 2018, NXP
#
# SPDX-License-Identifier: Apache-2.0
#

zephyr_include_directories(.)

zephyr_library_sources(fsl_common.c)
zephyr_library_sources(fsl_common_arm.c)
zephyr_library_sources_ifdef(CONFIG_ADC_MCUX_LPADC		fsl_lpadc.c)
zephyr_library_sources_ifdef(CONFIG_COUNTER_MCUX_CTIMER		fsl_ctimer.c)
zephyr_library_sources_ifdef(CONFIG_COUNTER_MCUX_LPC_RTC	fsl_rtc.c)
zephyr_library_sources_ifdef(CONFIG_DMA_MCUX_LPC		fsl_dma.c)
zephyr_library_sources_ifdef(CONFIG_ENTROPY_MCUX_RNG		fsl_rng.c)
zephyr_library_sources_ifdef(CONFIG_GPIO_MCUX_LPC		fsl_gpio.c fsl_pint.c fsl_inputmux.c)
zephyr_library_sources_ifdef(CONFIG_I2C_MCUX_FLEXCOMM		fsl_i2c.c fsl_flexcomm.c)
zephyr_library_sources_ifdef(CONFIG_I2S_MCUX_FLEXCOMM		fsl_i2s.c fsl_flexcomm.c)
zephyr_library_sources_ifdef(CONFIG_MCUX_OS_TIMER		fsl_ostimer.c)
zephyr_library_sources_ifdef(CONFIG_SOC_FLASH_LPC		fsl_flashiap.c)
zephyr_library_sources_ifdef(CONFIG_SOC_FLASH_MCUX		fsl_iap.c)
zephyr_library_sources_ifdef(CONFIG_SPI_MCUX_FLEXCOMM		fsl_spi.c fsl_flexcomm.c)
zephyr_library_sources_ifdef(CONFIG_UART_MCUX_FLEXCOMM		fsl_usart.c fsl_flexcomm.c)
zephyr_library_sources_ifdef(CONFIG_WDT_MCUX_WWDT		fsl_wwdt.c)
