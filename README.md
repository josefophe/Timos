# Running Timos on Android Tutorial guide


# Unlocking the Power: Running Timos on Android with Qemu and Termux - A Command-Line Odyssey

During my internship with Nokia, I was fortunate to delve into the world of TiMos, the Telecoms IP Operating System. This experience not only allowed me to work hands-on with cutting-edge technology but also opened doors to exploring the accessibility of running TiMos on a mobile platform. In this article, I'll share my journey of running Timos on Android using Qemu, Termux, and command-line interfaces.

## Tool Setup and Overview

### Leveraging Termux for Development
Termux, a powerful terminal emulator for Android, provided a Linux-like environment essential for development. Its flexibility and extensive package support turned my Android device into a command-line powerhouse. To begin, install Termux for Android using the official release available [here](https://github.com/termux/termux-app/releases). Once installed, you're ready to transform your Android device into a development hub.

### Qemu Configuration for Timos
Qemu, a versatile emulator, played a crucial role in emulating the necessary environment for Timos to run on Android. Configuring Qemu involved [To-do]. If you haven't installed Qemu on Termux yet, you can follow this detailed guide [^1^] to get started.

### Command-Line Magic
The command line became my playground, where I executed, monitored, and debugged the entire process. To create a Qemu x86_64 command for Timos, use the following:

```bash
qemu-system-x86_64 -cpu qemu64 -smp sockets=1,cores=2,threads=2 -m 1920M -hda /data/data/com.termux/files/home/storage/shared/Documents/TiMOS-SR-12.0.R6-vm/vm/7xxx-i386/sros-vm.qcow2 -device i82557b,netdev=n0 -netdev user,id=n0,dns=127.0.0.1 -boot c -rtc base=2023-08-10t00:05:00 -vnc :2 -nographic
```

This command initiates the Qemu system with specific configurations to run Timos on Android. Adjust the paths and parameters according to your setup.

## Testing and Iteration

With the tools in place, it was time to put everything to the test. Qemu allowed me to emulate different scenarios, while Termux served as the development hub. [To-do]

## Results and Observations

The moment of truth arrived as I witnessed Timos running seamlessly on my Android device. The results were not only satisfying but opened up possibilities for further exploration. 

![alt text](https://github.com/josefophe/Timos/blob/main/images/4.jpeg?raw=true) ![alt text](https://github.com/josefophe/Timos/blob/main/images/6.jpeg?raw=true)

![alt text](https://github.com/josefophe/Timos/blob/main/images/1.jpeg?raw=true) ![alt text](https://github.com/josefophe/Timos/blob/main/images/3.jpeg?raw=true)

## Challenges and Solutions

Every journey has its hurdles, and mine was no exception. From compatibility issues to unforeseen obstacles, I encountered several challenges along the way. Here's a glimpse into the challenges faced and the ingenious solutions that unfolded.

- Low RAM device will crash on running Qemu

## Lessons Learned

Reflecting on the journey, I gained not only technical insights but also a deeper understanding of the capabilities of Qemu, Termux, and the Android environment. These are the lessons I took away from this unique experience. [To-do]

In conclusion, running Timos on Android with Qemu and Termux proved to be an enlightening adventure. The convergence of telecom and Android ecosystems showcased the power of open-source tools and the endless possibilities they offer to innovative minds. During my internship with Nokia, the combination of working with Timos and exploring its adaptability on mobile platforms made the experience both enriching and accessible. If you're ready to dive into the world of command-line magic and push the boundaries of what's possible on your Android device, this journey is waiting for you.

[^1^]: To install Qemu in Termux, follow this detailed guide available [here](https://joyzonetech.blogspot.com/2021/05/How-To-Use-Qemu-In-Android.html).

