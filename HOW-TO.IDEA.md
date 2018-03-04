# How to Setup IntelliJ IDEA for This Project

Here is a brief set of instructions for setting up your IntelliJ IDEA installation to build the
[intellij-sdk-docs](https://github.com/JetBrains/intellij-sdk-docs) project, and run the demos.
They build on the instructions in the IntelliJ Platform SDK docs that describe
[how to checkout and build](www.jetbrains.org/intellij/sdk/docs/basics/checkout_and_build_community.html)
the [IntelliJ IDEA CE](https://github.com/JetBrains/intellij-community) project.

These instructions have been tested against the following versions of IntelliJ IDEA:
- IntelliJ IDEA 11.0.2 Community Edition
- IntelliJ IDEA 2016.3.7 Community & Ultimate Editions
- IntelliJ IDEA 2017.3.4 Community & Ultimate Editions

## Initial conditions

We will assume that you have already installed either IntelliJ IDEA Community or IntelliJ IDEA
Ultimate. If you're not sure which edition to install, start with IntelliJ IDEA Community. It's 
free, and it represents the most basic reference platform for the IntelliJ Platform SDK. IntelliJ
IDEA Ultimate can do everything that IntelliJ IDEA Community can do, and then some, so it is easy to
upgrade later on. From now on, when our discussion applies equally well to either edition, we will
drop the edition qualifier, and refer to the application as simply "IntelliJ IDEA".

We will also assume that you have a pristine installation of IntelliJ IDEA. In other words, you are
starting with factory-default settings. So, for example, you haven't defined a JDK yet for your
IntelliJ IDEA instance. If you don't actually have a pristine set of factory-default settings in
place, not to worry. But: you will have to tweak these instructions a bit here and there on the fly,
to adapt to your particular situation.

## Configuring IntelliJ IDEA before opening the project for the first time

Start your IntelliJ IDEA instance, but do not open a project. Instead, leave it at the welcome
screen. You'll notice a drop-down menu labeled "Configure" in the bottom right of the window. We'll
be using that several times, to establish a "global" set of IntelliJ IDEA settings that will apply
to all of your projects, including this one.

In Configure -> Plugins:
1. Ensure plugin “Kotlin” by Jetbrains is installed and enabled.
1. Ensure plugin “Gradle” by JetBrains is installed and enabled.
1. Ensure plugin “Grammar-Kit” by JetBrains is installed and enabled.
1. Ensure plugin “Docker integration” by JetBrains is installed and enabled (if available).
1. Ensure plugin “Ruby” by JetBrains is installed and enabled (if available).

In Configure -> Project Defaults -> Project Structures -> SDKs:
1. Create a JDK named “IDEA jdk”.
2. Point it at an installation of JDK 1.8.

In Configure -> Project Defaults -> Project Structure -> SDKs: 
1. Create an IDEA Platform Plugin SDK named "IDEA plugin sdk".
1. You will be prompted to use the installation of the running IDEA instance. Go ahead and do that.
1. When prompted for a JDK, select “IDEA plugin sdk”.

In Configure -> Project Defaults -> Project Structure -> SDKs:
1. If you do not have the Ruby plugin installed and enabled, skip this step.
1. Create a Ruby SDK named “IDEA ruby sdk”.
1. Point it at an installation of Ruby 2.0 or above.

Remarks:
- The JDK named "IDEA jdk" is the same one used 
  [to checkout and build](www.jetbrains.org/intellij/sdk/docs/basics/checkout_and_build_community.html) 
  the [IntelliJ IDEA CE](https://github.com/JetBrains/intellij-community) project.
- The IntelliJ Platform Plugin SDK named "IDEA plugin sdk" follows the same naming convention, for consistency.
- The Ruby SDK named "IDEA ruby sdk" also follows the same naming convention, again for consistency.
- Not all versions or editions of IntelliJ IDEA are compatible with some of the plugins used by this
  project; most notably the Docker and Ruby plugins.

## Configuring IntelliJ IDEA after opening the project for the first time

## Achieving your first clean build of the project within IntelliJ IDEA

## Running the demos from within IntelliJ IDEA

