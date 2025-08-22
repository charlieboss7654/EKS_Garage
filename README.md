# EKS Garage Vehicle Spawner

A dynamic and immersive vehicle spawning system for FiveM using `ox_target`. Perfect for realistic depots, public service fleets, or roleplay garages.


## Features

- AI Mechanic Peds
- Custom UI menu with detailed vehicle info
- Vehicles spawn in predefined parking spots
- Temporary blip (10 seconds) shows spawn location
- Global mechanic blips for all ped locations
- Easy Configuration

## Configuration

Edit `shared/config.lua` to define mechanics, vehicles, and spawn points.

## Example:

Config.Mechanics = {
    {
        label = "Main Depot",
        coords = vector3(-368.73, -127.92, 38.70),
        heading = 160.0,
        pedModel = "s_m_y_xmech_02",

        vehicles = {
            Utility = {
                {
                    title = "Tow Truck",
                    description = "Heavy-duty tow truck for vehicle recovery.",
                    make = "MTL",
                    model = "tow",
                    plate = "TOW001",
                    spawncode = "tow",
                    livery = 0
                },
                {
                    title = "Flatbed",
                    description = "Flatbed for transporting vehicles.",
                    make = "MTL",
                    model = "flatbed",
                    plate = "FLT001",
                    spawncode = "flatbed",
                    livery = 1
                }
            },
            Emergency = {
                {
                    title = "Ambulance",
                    description = "Basic life support ambulance unit.",
                    make = "Brute",
                    model = "ambulance",
                    plate = "AMB001",
                    spawncode = "ambulance",
                    livery = 0
                }
            }
        },

        parkingSpots = {
            { coords = vector3(-382.35, -137.42, 38.6), heading = 180.0 },
            { coords = vector3(-384.00, -137.50, 38.6), heading = 180.0 },
        }
    }
}

## Installation
Drag and drop the folder into your resources/ directory.

Add the following to your server.cfg:

ensure EKS_Garage

## Dependencies

ox_lib
ox_target

Ensure both are installed and started before this script.

## Support
Need help or want custom modifications?

Open a ticket at https://discord.gg/busQ9w6dqa

## License
This script is for personal or server use only unless otherwise licensed through EKS. Redistribution or resale is prohibited.
