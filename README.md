# BornTobeRoot

## Table of Contents
1. [Virtualization and Virtual Machine](#virtualization-and-virtual-machine)
2. [Difference between Debian and Rocky Distros](#difference-between-debian-and-rocky-distros)
3. [TTY](#tty)
4. [AppArmor](#apparmor)
5. [Sudo](#sudo)
6. [SSH](#ssh)
7. [UFW](#ufw)
8. [Creating Secure Passwords, Users, and Groups](#creating-secure-passwords-users-and-groups)
9. [Cron Expressions and crontab](#cron-expressions-and-crontab)
10. [Creating a Monitoring Script](#creating-a-monitoring-script)

---

## Virtualization and Virtual Machine

Virtualization is the process of creating a virtual version of a resource (like a server, operating system, storage device, or network) using software. This allows you to run multiple virtual machines (VMs) on a single physical machine.

A Virtual Machine (VM) is a software emulation of a physical computer that can run its own operating system and applications as if it were a physical machine.

To set up virtualization, you can use software like VMware, VirtualBox, or KVM (Kernel-based Virtual Machine). These tools allow you to create and manage virtual machines on your system.

## Difference between Debian and Rocky Distros

- **Debian**: Debian is one of the oldest and most stable Linux distributions. It uses the APT package manager and focuses on stability, security, and free software principles.

- **Rocky Linux**: Rocky Linux is a newer distribution, designed to be a direct replacement for CentOS after CentOS 8's shift towards CentOS Stream. It aims to provide a stable, free, and community-supported alternative to RHEL.

## TTY

TTY stands for TeleTYpewriter and refers to the command-line interface in Unix-like operating systems. It provides a text-based interface to interact with the system. When you log in to a terminal session, you are essentially accessing a TTY.

## AppArmor

AppArmor is a Linux security module that confines programs to a limited set of resources. It allows you to define per-program profiles, which restrict what specific programs can do. This provides an additional layer of security by limiting the potential damage that a compromised program can cause.

To install AppArmor on Debian-based systems, you can use the following command:

```bash
sudo apt-get install apparmor
```

## Sudo

Sudo is a command that allows users to run programs with the security privileges of another user, typically the superuser (root). This enables users to perform administrative tasks without having to log in as the root user.

To install sudo on Debian-based systems, you can use the following command:

```bash
sudo apt-get install sudo
```

## SSH

SSH (Secure Shell) is a cryptographic network protocol that allows secure communication over an unsecured network. It is commonly used for remote access to servers and for transferring files securely.

To install SSH on Debian-based systems, you can use the following command:

```bash
sudo apt-get install openssh-server
```

## UFW

UFW (Uncomplicated Firewall) is a user-friendly front-end for managing iptables, the default firewall management tool in Linux. It provides an easy-to-use interface for configuring firewall rules.

To install UFW on Debian-based systems, you can use the following command:

```bash
sudo apt-get install ufw
```

## Creating Secure Passwords, Users, and Groups

To create a secure password, it's recommended to use a combination of uppercase and lowercase letters, numbers, and special characters. Avoid using easily guessable information like names or common words.

To create a user, you can use the `adduser` command:

```bash
sudo adduser username
```

To create a group, you can use the `addgroup` command:

```bash
sudo addgroup groupname
```

## Cron Expressions and crontab

Cron is a time-based job scheduler in Unix-like operating systems. It allows you to schedule tasks to run at specific times or intervals. Cron expressions define when a task should be executed.

To edit the cron table for a user, you can use the `crontab -e` command:

```bash
crontab -e
```

Then, you can add your cron expressions and corresponding commands.

## Creating a Monitoring Script

To create a monitoring script using a shell file, you can follow these steps:

1. Create a new file with a `.sh` extension, for example `monitor.sh`.
2. Add your monitoring commands and logic to the script.
3. Make the script executable with the command:

```bash
chmod +x monitor.sh
```

You can then run the script using:

```bash
./monitor.sh
```

Make sure to include any necessary shebang line (e.g., `#!/bin/bash`) at the beginning of your script to specify the interpreter.

---
