# SilkwormConfigs
Printer configuration files for the Grasshopper plugin Silkworm.

## HOWTO: Write ini's for Silkworm

If you have an older version of Slic3r, export a setup from there and you are good to go.

If you don't have an older version of Slic3r, start out with the reference ini below and remove all comments. Most settings doesn't matter, even the ones that are not marked as defined by Silkworm. The important ones are the `start_gcode` and `end_gcode`.

Silkworm can't parse comments, so remove them all (`# comment` or `; comment`).

`start_gcode` and `end_gcode` are strings where newlines are written using `\n`. You can add comments here, using the `; comment` syntax.

## Reference ini
```ini
absolute_extrudersteps = 1                              # not defined in silkworm
acceleration = 0                                        # used as default_acceleration?
bed_size = 200,200                                      # not defined in silkworm, always set to Point3d(200, 200, 120)
bed_temperature = 60
bridge_fan_speed = 100
bridge_flow_ratio = 1
bridge_speed = 20
brim_width = 3                                          # not defined in silkworm
complete_objects = 0                                    # not defined in silkworm
cooling = 0
disable_fan_first_layers = 1
duplicate = 1                                           # not defined in silkworm
duplicate_distance = 6                                  # not defined in silkworm
duplicate_grid = 1,1                                    # not defined in silkworm
end_gcode = M104 S0 ; turn off temperature\nG28 X0  ; home X axis\nM84     ; disable motors # string
external_perimeter_speed = 100%                         # not defined in silkworm
extra_perimeters = 1                                    # not defined in silkworm
extruder_clearance_height = 20
extruder_clearance_radius = 20
extruder_offset = 0x0                                   # not defined in silkworm
extrusion_axis = E                                      # not defined in silkworm
extrusion_multiplier = 1                                # not defined in silkworm
extrusion_width = 0                                     # not defined in silkworm
fan_always_on = 0                                       # not defined in silkworm
fan_below_layer_time = 60                               # not defined in silkworm
filament_diameter = 1.75
fill_angle = 45
fill_density = 0.4
fill_pattern = rectilinear                              # string
first_layer_bed_temperature = 60
first_layer_extrusion_width = 200%                      # not defined in silkworm
first_layer_height = 100%
first_layer_speed = 20%
first_layer_temperature = 185
infill_acceleration = 50
infill_every_layers = 1
infill_extruder = 1                                     # not defined in silkworm
infill_extrusion_width = 0                              # not defined in silkworm
infill_speed = 20
layer_gcode =                                           # not defined in silkworm
layer_height = 0.5
max_fan_speed = 100                                     # not defined in silkworm
min_fan_speed = 35                                      # not defined in silkworm
min_print_speed = 10
nozzle_diameter = 0.5
output_filename_format = [input_filename_base].gcode    # not defined in silkworm
perimeter_acceleration = 25
perimeter_extruder = 1                                  # not defined in silkworm
perimeter_extrusion_width = 0                           # not defined in silkworm
perimeter_speed = 20
perimeters = 3
post_process =                                          # not defined in silkworm
print_center = 100,100                                  # not defined in silkworm
randomize_start = 1                                     # not defined in silkworm
retract_before_travel = 2
retract_length = 1
retract_lift = 0
retract_restart_extra = 0
retract_speed = 30
rotate = 0                                              # not defined in silkworm
scale = 1                                               # not defined in silkworm
skirt_distance = 6
skirt_height = 1
skirts = 1
slowdown_below_layer_time = 15                          # not defined in silkworm
small_perimeter_speed = 20
solid_fill_pattern = rectilinear                        # string
solid_infill_speed = 20
solid_layers = 3
start_gcode = G28 ; home all axes
support_material = false                                # defined in silkworm, not in example, boolean
temperature = 185                                       # not defined in silkworm
top_solid_infill_speed = 20                             # not defined in silkworm
travel_speed = 100
use_relative_e_distances = 0                            # not defined in silkworm
xbar_heightfromnozzletip = 30
xbar_width = 30
z_offset = 0
```
