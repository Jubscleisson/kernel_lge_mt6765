#
# Makefile for the i2c core.
#

obj-$(CONFIG_I2C_BOARDINFO)	+= i2c-boardinfo.o
obj-$(CONFIG_I2C)		+= i2c-core.o
obj-$(CONFIG_I2C_SMBUS)		+= i2c-smbus.o
ifneq ($(TARGET_BUILD_VARIANT),user)
obj-$(CONFIG_I2C_CHARDEV)	+= i2c-dev.o
endif
obj-$(CONFIG_I2C_MUX)		+= i2c-mux.o
obj-y				+= algos/ busses/ muxes/
obj-$(CONFIG_I2C_STUB)		+= i2c-stub.o
obj-$(CONFIG_I2C_SLAVE_EEPROM)	+= i2c-slave-eeprom.o

ccflags-$(CONFIG_I2C_DEBUG_CORE) := -DDEBUG
CFLAGS_i2c-core.o := -Wno-deprecated-declarations
