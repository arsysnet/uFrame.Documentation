# Commands

Commands allow to change the state of the ViewModel that the Element represents. If player gets damage, the TakeDamage command can be executed to descrease the player’s health. Usually, the ViewModel data should not be changed directly but only through the use of the defined commands. There are however use cases where VMs data can be changed directly from the View with [Scene Properties](SceneProperties) or [Services](Services).

[link to an example]

The actual implementation of the command is not stored inside the ViewModel but inside its [Controller](Controllers). When a ViewModel’s command gets called, it executes the command’s implementation defined in the controller. The controller then changes the ViewModel data what next triggers [bindings](Bindings) defined in the View.

![](https://dl.dropboxusercontent.com/u/75445779/uFrame_wiki/uFrame_MVVM_flow.png)