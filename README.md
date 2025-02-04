# Coreboot ThinkPad W500

Here's VGA bios's along with coreboot rom's I compiled for the W500(T500 should work, as the GPUs are esssentialy the same aside from memory). SeaBIOS was used as the ATI card needs a VGA bios to initialize. Using nvramtool you can switch between 'Integrated Only', 'Discrete Only' or 'Dual Graphics'

For example, nvramtool -w "hybrid_graphics=Integrated Only"

Now for the issues:
- Using Integrated/Dual Graphics mode will cause the display to be blank during boot until linux takes over.
- Windows 7/10 both throw an ACPI BSOD on boot, making linux your only option.
- After flashing, you'll default to integrated only. This means you should make a Linux drive prior with radeon firmware using the stock bios. Not even grub will be visible. I would just switch to Discrete Only if I had to install another distro.

# What rom should I use?

nw500cbrv1.rom is the last/final rom I've made for the moment. The others were trial and error, do not use them(besides bios_orig.rom which is the OEM bios.)

This will give you the ability to run Core 2 Quad's like the T400/T500(Pin removal/one soldered wire still required). Be aware, they will run at 45w TDP and hybrid mode will activate BOTH graphics cards. I'm not sure how well that combo will work, you may encounter throttling or overheating. Normally the W500 switches between one card or the other in Windows 7. I'm not responsibile for any issues you encounter.
