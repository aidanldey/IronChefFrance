# Clock Quest

A single-file HTML app that teaches children to read an analog clock.

Open `index.html` in any browser. No build step, no server, no dependencies.

## The idea

Two visual scaffolds do the teaching:

- **Twelve colored hour stripes.** Each stripe covers the whole hour, running from
  one number to the next — so the yellow "3" stripe stretches from 3 o'clock to
  4 o'clock. Wherever the short hand is standing, that stripe's number *is* the
  hour. This removes the classic mistake of reading 3:30 as "half past four".
  The short hand carries a tip dot painted in its stripe's color, so even a hand
  resting exactly on a dividing line still says which hour it means.
- **An outer minute ring, 0 to 59.** It is split into twelve five-minute blocks
  tinted to match the hour stripes, with a tick for every single minute and a
  number on every fifth one.

## The seven steps

Each lesson unlocks the next and follows the same shape: pop-up teaching cards →
worked examples that explain themselves one step at a time → *set the clock to
this time* → *now tell me the time*.

1. **Meet the Clock** — the two hands, the stripes, the ring, and a free play round
2. **O'clock** — the long hand straight up at the 12
3. **Half past** — the long hand at the 6, and why the hour does not change yet
4. **Quarter past & quarter to** — the long hand at the 3 and the 9
5. **Counting by fives** — every block on the ring is five minutes
6. **Every single minute** — using the tiny ticks
7. **Clock Champion** — training colors off, numbers moved to their real-clock
   positions

Stars are awarded per lesson (three for a clean run) and progress is kept in
`localStorage`.

## Details worth knowing

- The hands are draggable with a mouse or finger. They can also be moved with the
  arrow keys after picking a hand, and `h` / `m` switch between them.
- The hour hand drifts through its stripe as the minutes advance, exactly as a
  real clock does — at half past it sits in the middle of the stripe.
- Three toggles under the clock: color stripes on/off, a number on every minute,
  and real-clock numbering.
- Wrong answers get a targeted hint, the relevant part of the face flashes, and a
  **Show me how** button walks through the reading step by step.
- Times are read back in words as well as digits ("twenty-three minutes to three"),
  so *past* and *to* are learned alongside the digital form.
