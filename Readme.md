
# What is this

A collection of property sheets for inclusion in Visual Studio projects.
They make projects (.vcxproj) more readable and easier to maintain
by addressing specific aspects (for example use of precompiled headers
or linking with an external library) in separate files named corresponding
to the aspect. They can be freely combined to determine the whole project.

# How to use

Include property sheets in project files (.vcxproj) in the ImportGroup
labeled 'PropertySheets' as in this example:

    <ImportGroup Label="PropertySheets">
        <Import Project="precompiled_headers.props"/>
    </ImportGroup>

Eliminate corresponding settings made directly in the .vcxproj file by
Visual Studio. In the long run, begin to think of .vcxproj as a filetype
to be edited manually - dont't let Visual Studio write it!

# Status

Only examples so far.

# Examples

SubsystemConsole.props
: Used by projects intended for the console. Defines the subsystem and corresponding preprocessor definitions.

SubsystemWindows.props
: Used by GUI-Projects. Defines the subsystem and corresponding preprocessor definitions.

LuaForWindows.props
: Used to include Lua installed by [LuaForWindows](https://github.com/rjpcomputing/luaforwindows)

precompiled_headers.props
: Used to configure the use of precompiled headers. Makes it easy to adapt the name of the header or the pch-file.