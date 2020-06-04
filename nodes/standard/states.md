# States
The **States** node is used to represent logical states visually. You can define your own states and values, each state will then have unique settings for these values and the node will transition between these settings as the state is changed. To learn more take a look at the [guide](/guides/switch.md).

<div class="ndl-images">
    <img src="/nodes/standard/states.png" class="ndl-image med">
</div>

<div class = "node-inputs">

## INPUTS
**States**  
A state node can have as many states as is necessary. Add a new state by clicking on the plus button.

**Values**  
Every state will have its own set of values. All values need to be set for every state that is added.

<div class="ndl-images">
    <img src="/nodes/standard/states-example.png" class="ndl-image small"></img>
</div>

**State**
This is the starting state for the state node when it is created. You can also connect to the input to force the state.

**Toggle**
 Will animate to the next state, or the first state if the current state is the last one.

## Value types
For each value you can specify the type. Default is **Number**.

<div class="ndl-images">
    <img src="/nodes/standard/states-value-types.png" class="ndl-image small"></img>
</div>

## State values
For every state you can specify each of the values. This is the value that they will have whey you are at that specific state.

<div class="ndl-images">
    <img src="/nodes/standard/state-values.png" class="ndl-image small"></img>
</div>

## State transition
Here you specify if there should be a transition to the target state. So when you switch to the given state it will transition smoothely over time.

<div class="ndl-images">
    <img src="/nodes/standard/state-transition.png" class="ndl-image small"></img>
</div>

**Easing Curve**
Selects the curvature of the state transition animation. Can be **Ease Out** (default), **Ease In**, **Linear**, **Ease In Out** and **Cubic Bezier**. If you choose the latter, you can use this [tool](https://cubic-bezier.com/) to generate the control points.

**Duration**  
The duration of the state animation. How long it takes in milliseconds to go from the previous state to this state.

## To state actions
Each state will have a signal input called **To** followed by the state name. This can be used to connect a signal that will take the states node to that state when the signal is triggered.

</div>

<div class = "node-outputs">

## OUTPUTS

**State**  
The name of the current state

**State Changed**  
A signal that is sent when the current state is changed

**Values**  
All of the values for the current state

**At "State X"**  
True when the current selected state is X

**Has Reached "State X"**  
Signal that is being sent when the state animation to state X is complete

</div>