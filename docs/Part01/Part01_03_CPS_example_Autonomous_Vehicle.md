# CPS Example: Autonomous Vehicle

An [Autonomous Vehicle](wiki:Self-driving_car) is a car that is capable of operating with *reduced* or *no human input*. There are different levels of autonomy, which will be discussed later in the lecture materials.

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/HS1wV9NMLr8?si=3-GvXxwGKglwEJw2"
    title="How AI Helps Autonomous Vehicles See Outside the Box"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>


An autonomous vehicle must be aware of its environment, achieved by an array of sensors (including but not limited to):
- Cameras: multiple RGB cameras are attached to a vehicle, capturing images and video like human eyes,
- [LiDAR, or light Detection And Ranging](wiki:Lidar): a method for determining [ranges](https://en.wikipedia.org/wiki/Length_measurement#Ranging) by targeting an object or a surface with a [laser](wiki:Laser) and measuring the time for the reflected light to return to the optical receiver.
- [GPS, or Global Positioning System](wiki:Global_Positioning_System): provides [geolocation](wiki:Geopositioning) and [time information](wiki:Time_and_frequency_transfer),
- [Radar](wiki:Radar): a system that uses [radio waves](wiki:Radio_wave) to determine the distance [ranging](https://en.wikipedia.org/wiki/Length_measurement#Ranging), direction, and [radial velocity](wiki:Radial_velocity) of objects relative to the site,
- [Ultrasound](wiki:Ultrasound): to detect the presence of an object.