# Kobra Plus Klipper Config
#### consider everything here a work in progress

You need to move [R65 to R66](https://klipper.discourse.group/t/anycubice-kobra-max-config-file/5379/8) or don't even bother continuing here.

Install a built HC32F460 firmware for `HC32F460_SERIAL_PA3_PA2` ("Anycube") per the standard [Klipper installation instructions](https://www.klipper3d.org/Installation.html).

# Here's some info on what I did and why

Anycubic put three TMC2209 stepper drivers (X/Y/Z) and a single TMC2208 as E. Configs I found didn't seem to follow advice from the [TMC drivers instructions](https://www.klipper3d.org/TMC_Drivers.html)

Started with a config somewhat comprised of things found on reddit posts and the above klipper discourse page. Nothign I found worked well for me, or had additional stuff like some external screen. Fair warning: the screen on the Anycubic Kobra Plus is not going to do anything with this firmware. Everything you do will be through Octoprint.

Before disabling stealthChop in favor of spreadCycle (and disabling interpolate) per the [TMC drivers instructions](https://www.klipper3d.org/TMC_Drivers.html) I had all kinds of [really bad Y layer shift](https://i.imgur.com/TIiYeVy.jpg). Per those TMC driver instructions, increasing microsteps would quiet the stepper drivers down if you switch to spreadCycle, that worked. Z wouldn't, however, play nice (I probably need to just adjust its rotation_distance, but that's low priority).

#### Enjoy
