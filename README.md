![License](https://img.shields.io/github/license/intuit/sdp)

# SDP - a scalable size unit
An android lib that provides a new size unit - sdp (scalable dp). This size unit scales with the screen size. It can help Android developers with supporting multiple screens.
This fork uses 390 as a baseline, providing consistent measurements between material design guidelines and sdp size on a regular modern phone.

# Attention
Use it carefully! for example, in most cases you still need to design a different layout for tablets.

# Example
[Here](https://github.com/intuit/sdp/blob/master/sdp-android/src/main/res/layout/sdp_example.xml) is a single layout built using sdp:

![sdp example](https://github.com/intuit/sdp/blob/master/sdp_example.png)

And [here](https://github.com/intuit/sdp/blob/master/sdp-android/src/main/res/layout/dp_example.xml) is the same layout built using dp:

![dp example](https://github.com/intuit/sdp/blob/master/dp_example.png)

You can see that sdp scales with the screen size and the dp stays with the same size on all screen sizes.

# Getting Started

To add sdp to your project:

* Download this repository as ZIP file
* Unzip it
* Copy the content from Res folder to your project res folder
* enjoy

By default the library has measurements from 1sdp to 600 sdp, and negative measurements from -1sdp to -60sdp

If you want a liter version you can download the [Lite](https://github.com/elMuso/sdp-modern/archive/refs/heads/lite.zip) branch, it goes from 1sdp to 60 sdp, and doesn't include negative units. You can get them 
programatically by using `context.resources.getDimension(R.dimen._1sdp) * your_desired_size` in kotlin or `getContext()-getResources().getDimension(R.dimen._1sdp) * your_desired_size;` in java

For easy mapping of designs to sdp units, one can create designs with 390 pixels screen width - in this case each pixel in the design corresponds to 1 sdp.

# Note
The sdp size unit calculation includes some approximation due to some performance and usability constraints.
