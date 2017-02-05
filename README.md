# NUKE BRICKER

Nuke Gizmo for supervising shots.

# Usage
### [Video Tutorial](https://youtu.be/z18xjO2nJfg)

### [Tricks](https://youtu.be/TFQaIXKqf1Q)

# Install

1. Copy this code to __menu.py__

    ```python
    import nuke
    
    toolbar = nuke.toolbar("Nodes")
    toolbar.addCommand( "Merge/Bricker", "nuke.createNode(\"pw_bricker\")", icon="bricker.png")
    def install_bricker():
        nuke.thisNode()['mainScript'].execute()
        nuke.removeOnCreate(install_bricker, nodeClass='pw_bricker')
    nuke.addOnCreate(install_bricker, nodeClass='pw_bricker')
    
    #fix overlay action
    nuke.menu('Viewer').items()[1].action().setChecked(True)
    ```

2. Copy __bricker.png__ to NUKE_PATH

3. Restart Nuke


# known issues

1. Not work in Properties panel yet. Use floating  panel.

2. Break connection when copy\paste
