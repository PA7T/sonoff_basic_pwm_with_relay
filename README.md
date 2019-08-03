# Sonoff basic pwm with relay
Homekit firmware for the Sonoff basic module to control a PWM dimmable power supply

# This is an example for esp-homekit-demo
Demo of [Apple HomeKit accessory server
library](https://github.com/maximkulkin/esp-homekit).

## Usage

See [build instructions](https://github.com/maximkulkin/esp-homekit-demo/wiki/Build-instructions)

Then build it by running

```console
docker run -it --rm -v `pwd`:/project -w /project esp-rtos make -C sonoff_basic_pwm_with_relay all
```
Then flash it (and optionally immediately run monitor)

```console
docker run -it --rm -v `pwd`:/project -w /project --device=/dev/ttyUSB0 esp-rtos make -C sonoff_basic_pwm_with_relay flash
```

NOTE: you can have the following helper function in  ~/.bashrc:

```console
docker-run() {
  docker run -it --rm -v $(pwd):/project -w /project "$@"
}
```

Then, to run a container I just do

```console
docker-run esp-rtos make -C sonoff_basic_pwm_with_relay all
```






