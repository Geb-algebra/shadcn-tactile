# shadcn-tactile

A shadcn/ui registry that makes interfaces feel tangible.

shadcn-tactile provides subtly three-dimensional components and expressive animations while preserving the familiar APIs and usage patterns of [shadcn/ui](https://ui.shadcn.com/).

Its goal is to make interfaces more intuitive and responsive without sacrificing simplicity, accessibility, or usability.

## Design Principles

### 1. Make Interactive Objects Feel Tangible

Interactive objects should look interactive.

shadcn-tactile uses subtle shadows, gradients, and highlights to give interactive elements a sense of physical depth. This helps users distinguish objects they can manipulate from those that simply display information.

- **Interactive objects** have a slightly raised or recessed appearance that suggests how they can be manipulated.
- **Non-interactive objects** generally remain flat, avoiding misleading visual affordances.
- **Overlay surfaces**, such as dialogs and popovers, may use elevation to communicate their position in the interface, independently of whether they are interactive.

Depth is intentionally restrained. The interface should feel tactile without becoming visually heavy or overly decorative.

### 2. Respond Naturally to Interaction

Interactive objects should provide immediate, meaningful feedback.

shadcn-tactile uses animations that resemble familiar physical responses:

- **Hover:** An interactive object may rise slightly, inviting interaction.
- **Press:** An object may move downward, creating the sensation of being pressed.
- **Focus:** An object clearly communicates keyboard focus.
- **Invalid:** An object may briefly shake to communicate a failed interaction.
- **Disabled:** An object communicates its unavailable state without suggesting that it can be manipulated.

Animations are subtle, brief, and consistent across components. Their purpose is to communicate interaction, not to attract attention unnecessarily.

### 3. Animate Changes in Objects and Layout

Changes to objects should be visually understandable.

shadcn-tactile uses animation to communicate when objects appear, disappear, move, or change size.

- **Creation:** An object may expand into view while fading in.
- **Deletion:** An object may collapse and fade out.
- **Movement:** An object may smoothly transition to its new position.
- **Layout changes:** Surrounding objects should smoothly reposition themselves when the layout changes.

These animations are not limited to interactive objects. Non-interactive objects can also animate to communicate changes in the interface.

Animations should help users follow what changed and where objects moved.

### 4. Use Motion with Restraint

Animation should always serve a purpose.

shadcn-tactile avoids continuous, excessive, or purely decorative motion. Static interfaces remain visually stable, and animations occur primarily in response to user interaction or meaningful state changes.

Motion should communicate behavior and preserve context without distracting users from their tasks.

### 5. Never Make Users Wait for Animation

Animations must not interfere with interaction.

Users should be able to continue interacting with the interface while animations are running. Repeated or rapid interactions should remain responsive, and animations should not unnecessarily delay state changes.

Visual feedback follows application behavior rather than becoming a prerequisite for it.

### 6. Support Light and Dark Themes

shadcn-tactile supports both light and dark appearances.

The two themes share the same principles of depth, interaction, and motion, but may use different visual techniques to achieve them.

- **Light theme:** Soft shadows and subtle highlights communicate elevation.
- **Dark theme:** Gentle surface gradients, highlights, and borders communicate depth where shadows alone may be insufficient.

Both themes aim to provide consistent affordances, clear visual hierarchy, and comfortable readability.

### 7. Preserve Accessibility

Visual richness must not compromise accessibility.

shadcn-tactile preserves accessible interaction patterns, visible keyboard focus, and appropriate disabled and invalid states.

Important information must never be communicated through animation, color, or elevation alone.

## Compatibility with shadcn/ui

shadcn-tactile is designed as a visual and motion-focused alternative to standard shadcn/ui components, not a new component API.

- **Familiar components:** Standard shadcn/ui component names and usage patterns are preserved.
- **Compatible APIs:** Existing props, variants, and component behavior are maintained wherever possible.
- **Minimal migration:** Applications using standard shadcn/ui components should require little or no application-level changes when adopting their shadcn-tactile counterparts.
- **Optional enhancements:** Features that require additional integration, such as animated list transitions, are provided separately rather than changing standard component contracts.

As with shadcn/ui, components are added directly to your project, allowing you to inspect, modify, and own their source code.

shadcn-tactile enhances how an interface looks and responds without prescribing how an application manages its data, state, or business logic.

## Philosophy

**Objects should look like what they are, respond to what users do, and move in ways that make changes understandable.**

shadcn-tactile combines the clarity of modern flat interfaces with subtle physical affordances and purposeful motion.

The result is an interface that feels responsive, tangible, and alive—without getting in the user's way.