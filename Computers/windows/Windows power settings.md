Power Options

Power management allows Windows to selectively reduce or turn off the power supplied to hardware components. The computer can be configured to enter a power-saving mode automatically; for example, if there is no use of an input device for a set period. This is important to avoid wasting energy when the computer is on but not being used and to maximize run-time when on battery power. The user can also put the computer into a power-saving state rather than shutting down.

The Advanced Configuration and Power Interface (ACPI) specification is designed to ensure software and hardware compatibility for different power-saving modes. There are several levels of ACPI power mode, starting with S0 (powered on) and ending with S5 (soft power off) and G3 (mechanically powered off). In between these are different kinds of power-saving modes:

- Standby **/Suspend to RAM**—Cuts power to most devices (for example, the CPU, monitor, disk drives, and peripherals) but maintains power to the memory. This is also referred to as ACPI modes S1–S3.
- Hibernate **/Suspend to Disk**—Saves any open but unsaved file data in memory to disk (as hiberfil.sys in the root of the boot volume) and then turns the computer off. This is also referred to as ACPI mode S4.

In Windows, these ACPI modes are implemented as the sleep, hybrid sleep, and modern standby modes:

- A laptop goes into the standby state as normal; if running on battery power, it will switch from standby to hibernate before the battery runs down.
- A desktop creates a hibernation file and then goes into the standby state. This is referred to as hybrid sleep mode. It can also be configured to switch to the full hibernation state after a defined period.
- Modern Standby utilizes a device's ability to function in an S0 low-power idle mode to maintain network connectivity without consuming too much energy.

You can also set sleep timers for an individual component, such as the display or hard drive, so that it enters a power-saving state if it goes unused for a defined period.

The **Power & sleep** settings provide an interface for configuring timers for turning off the screen and putting the computer to sleep when no user activity is detected. The Control Panel **Power Options** applet exposes additional configuration options.

One such option is defining what pressing the power button and/or closing the lid of a laptop should perform (shut down, sleep, or hibernate, for instance).

![](https://s3.amazonaws.com/wmx-api-production/courses/35011/images/8289-1639514851191-windows_10_21h2_control_panel_power_options_button.png)

Configuring power settings via the Power Options applet in Control Panel. (Screenshot courtesy of Microsoft.)

You can also use the Power Options applet to enable or disable fast startup. This uses the hibernation file to instantly restore the previous system RAM contents and make the computer ready for input more quickly than with the traditional shutdown option.

If necessary, a more detailed **power plan** can be configured via Power Options. A power plan enables the user to switch between different sets of preconfigured options easily. Advanced power plan settings allow you to configure a very wide range of options, including CPU states, search and indexing behavior, display brightness, and so on. You can also enable **Universal Serial Bus (USB) selective suspend** to turn off power to peripheral devices.