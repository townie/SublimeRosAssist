# SublimeRosAssist
A simple sublime-text-3 plugin that make life easier for handling ROS projects

## Install

Clone this repo to  `~/.config/sublime-text-3/Packages` or your own sublime config folder.

## Main Functions

### SublimeRosAssistRevealPackage ###

Usage: input `rosassistrevealpackage` in `command palette` or call `sublime_ros_assist_reveal_package` in `run_commands()`

Description: scan the project folders, find ros workspace, list all catkin packages, expand the choosen package in the side bar.

### SublimeRosAssistGenerateClangFlags ###

Usage: input `rosassistgenerateclangflags` in `command palette` or `call sublime_ros_assist_generate_clang_flags` in `run_commands()`

Description: scan the project folders, find ros workspace, scan all catkin packages, generate compile flags for clang consists of:

1. [extra_flags_for_clang](https://github.com/groundmelon/SublimeRosAssist/blob/master/sublime_ros_assist.sublime-settings#L2) in the [sublime_ros_assist.sublime-settings](https://github.com/groundmelon/SublimeRosAssist/blob/master/sublime_ros_assist.sublime-settings) as general compile flags;
2. `${CATKIN_WORKSPACE_DIR}/devel/include` as the include flags (`-I`);
3. all the include folders in the scanned packages as include flags (`-I`);
 
and add the flags to `sublimeclang_options` in the project settings for getting [SublimeClang](https://github.com/quarnster/SublimeClang) to work properly.

### SublimeRosAssistShowYcmExtraConf ###

Usage: input `rosassistshowycmextraconf` in `command palette` or call `sublime_ros_assist_show_ycm_extra_conf` in `run_commands()`

Description: It will open up a new tab contains an example for ycm\_extra\_conf.py using in [C++YouCompleteMe](https://github.com/glymehrvrd/CppYCM).
