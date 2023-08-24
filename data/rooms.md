# Room Definition Failes
Room definition files MUST be stored in the [TOML] format and contain the following variables:

| Key | Data type | Optional | Notes |
| --- | --------- | -------- | ----- |
| room_id | integer | No | |
| short_desc | string | No | |
| long_desc | string | No | |
| sights | map<string, string> | Yes | |
| sounds | map<string, string> | Yes | |
| smells | map<string, string> | Yes | |
| exits | map<string, integer> | Yes | |

## Variable Description
room_id: a unique integer used to identify the room within the game system
short_desc: a short descriptor used as a title in verbose mode and as the description of the room in compact mode.
log_desc: an indepth description of the room used in verbose mode.
sights: a list of things that the players can look at, along with their associated descriptions.
sounds: a list of things that the players can listen to, along with their associated descriptions.
smells: a list of things that that players can smell, along with their associated descriptions.
exits: a list of exits from this room by their exit commands, along with the room they are attached to.
