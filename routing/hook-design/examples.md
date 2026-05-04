# Hook Design Examples

Use these examples to check whether `hook-design` is producing a stable handoff object.

These are diagnosis examples, not copy templates.

## Example 1: Generic Pain To `painRecognition`

Input:

```text
I want a stronger opening for a weight-loss product. Current line is: trying to lose weight?
```

Output:

```text
Hook goal: make stalled effort feel immediately personal
Audience state: frustrated after repeated failed attempts
Specific pain or desire: months of effort with no visible scale movement
Viewer self-identification cue: "I've been doing this for months and nothing changed"
Hook mechanism: painRecognition
Opening line or opening move: you've been trying to lose weight for 8 months and the scale hasn't moved
Listener reaction: wait, yes, that is exactly it
Problem deepening: the viewer has already spent effort and wants proof that this is not another reset
Product reveal rule: do not reveal the product in the opening line; reveal only after the stalled-effort problem is clearly established
Why this mechanism fits: the audience does not need more category awareness; they need immediate self-recognition
Success metric: the opening should make the viewer feel specifically seen before the product appears
Hook risks: too broad, too salesy, no self-recognition, product enters too early
Next handoff: visual-hook
```

## Example 2: Early Product Reveal To `socialOrIdentityStake`

Input:

```text
Frame one shows the bottle and the speaker says this changed my hair.
```

Output:

```text
Hook goal: create problem recognition before product recognition
Audience state: worried their hair still looks flat or oily even after styling
Specific pain or desire: visible hair issue that affects confidence before going out
Viewer self-identification cue: "my hair still looks off even when I already got ready"
Hook mechanism: socialOrIdentityStake
Opening line or opening move: haven't you noticed your hair can ruin the whole look even when the outfit is good
Listener reaction: exactly, that is the part nobody says out loud
Problem deepening: the mismatch between a polished look and one obvious flaw makes the problem socially legible
Product reveal rule: keep the bottle out of frame one and out of the opening line
Why this mechanism fits: the pain matters because of presentation and confidence, not because hair is an abstract category problem
Success metric: frame one should show the consequence clearly enough that the viewer feels the social cost before brand recognition
Hook risks: obvious ad detection, beauty-commercial polish, no lived-in problem cue
Next handoff: visual-hook
```

## Example 3: Benchmark-Led Leisure Opening To `questionGap`

Input:

```text
We have a benchmark of an attractive couple on paddleboards. We want that kind of opening energy for our leisure kit video.
```

Output:

```text
Hook goal: sell the desirable day before the item list begins
Audience state: browsing for aspirational leisure content, not actively shopping yet
Specific pain or desire: wanting an easy, social, outdoors day that feels relaxed and desirable
Viewer self-identification cue: "I want that exact kind of day"
Hook mechanism: questionGap
Opening line or opening move: start on a lived-in overhead leisure shot that makes the viewer ask where they are and what is on the board
Listener reaction: wait, what are they using out there
Problem deepening: the viewer wants the scene first and only then becomes curious about the setup details
Product reveal rule: do not lead with the kit inventory; let the scene earn the curiosity first
Why this mechanism fits: the audience is not shopping with high intent yet, so desire must create the question before the product can answer it
Success metric: the first beat should generate a concrete "what is in that setup" question without reading like a kit ad
Hook risks: scenery-only opening, product list too early, couple portrait drift, polished travel-ad feel
Next handoff: reference-decode
```

## Review Standard

The dry run is successful when:

- the `Hook Brief` shape stays consistent
- the mechanism is explicit instead of implied
- the next skill is obvious from the output
- downstream work does not need to re-guess the opening logic

## Ecosystem Note

More production skills, research workflows, and creative systems: [postplus.io](https://postplus.io)
