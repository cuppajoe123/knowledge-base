# Virtualization and Containerization

## What is virtualization
A key aspect of computer science is the idea of abstraction: hiding away the details of an application for the benefit of the user. Where your favorite programming language is just an abstraction of machine code, a virtual machine is simply an abstraction of the entire computer. It uses software to simulate another computer. Virtual machines have many use cases, both personal and enterprise. It allows you to have multiple computers on a single piece of hardware.

You could be using your main desktop operating system and decide that you want to try a new OS, without fully committing to it. You could spin up a virtual machine as they say, and begin messing around. If you break something, it doesn't matter because you can just go back to working on your main desktop, or create a new VM. So they are great for experimenting and trying new things.

Another use case is for servers. Say you have a power enterprise server, with 128GB of memory and 64 CPU cores. You have multiple services you need to run that have varying needs in terms of both software and hardware. You could buy a seperate server for each services, or you could provision different amounts of resources on your one server to each service within a seperate virtual machine. This comes with the added benefit that if one service is compromised, the others can keep running.

## Two categories of virtualization
- Virtual machines are run on top of a *hypervisor*. A hypervisor is used to run, create, destroy and otherwise manage your virtual machines.
- Hypervisors fall into two categories, Type 1 and Type 2.
- A type 1 hypervisor, sometimes called a native hypervisor, is installed directly onto the hardware, taking the place of a host operating system. A type 1 hypervisor could just be a specialized Linux distro where all non-essential features are removed. You can manage these hypervisors through the command line or sometimes a web interface.
- Type 2 hypervisors are application level programs that you can install like any other program. Type 2 hypervisors rely on a host operating system to run on. So the VMs are run on top of the hypervisor, which is in turn run on top of the host operating systems
- As an aside, the OS you are running inside the VM is called the guest operating system.
- When using VMs for server applications, Type 1 hypervisors are generally used.

## Examples
- Install Virtualbox (a Type 2 hypervisor) and create a Linux VM.
- Demonstrate Proxmox (a Type 1 hypervisor), both the commandline and the web console.
