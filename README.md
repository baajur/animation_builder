# animation_builder

Fluent and type-safe API to build keyframes and timing for Web Animation API

## Usage

A simple usage example:

```dart
void main() {
    final anim = new AnimationBuilder().duration(2000).fillForwards()
      ..createAt(0.0).backgroundColor('blue')
      ..createAt(1.0).backgroundColor('red');
    
    print(anim.makeKeyframes());
    print(anim.makeOptions());
    
    querySelector('#output').animate(anim.makeKeyframes(), anim.makeOptions());
}
```
