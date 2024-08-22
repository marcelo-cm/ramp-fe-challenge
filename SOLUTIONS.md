# Bug 1: Select dropdown doesn't scroll with rest of the page

We just have to use an absolute position instead of a fixed position

# Bug 2: Approve checkbox not working

There are two ways to solve this.

1. We use the `ref` to `click` the input on click of the parent `div`
2. We can change the `input` from `display: none;` to `opacity; 0` to obtain the same effect, then we position is in the center of the parent `div` by using the `flex` properties on its styling.

The former allows for better testing.
