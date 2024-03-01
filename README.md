# CCTV test

In creating a CCTV-like scene in Godot, using the Mobile profile, with a `WorldEnvironment`, I came across the spammed error

    E 0:00:00:0452   draw_list_bind_uniform_set: Attempted to use the same texture in framebuffer attachment and a uniform (set: 3, binding: 4), this is not allowed.
    <C++ Error>    Condition "attachable_ptr[i].texture == bound_ptr[j]" is true.
    <C++ Source>   drivers/vulkan/rendering_device_vulkan.cpp:7372 @ draw_list_bind_uniform_set()

The error does not show up when using the Forward+ profile.

**However**, the error shuts up using the Mobile IF I enable Glow in the `WorldEnvironment`. The error also goes away if I remove the `WorldEnvironment`, which is clearly not ideal.

In short: I'm confused.
