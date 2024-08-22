# Bug 1: Select dropdown doesn't scroll with rest of the page

We just have to use an absolute position instead of a fixed position

# Bug 2: Approve checkbox not working

There are two ways to solve this.

1. We use the `ref` to `click` the input on click of the parent `div`
2. We can change the `input` from `display: none;` to `opacity; 0` to obtain the same effect, then we position is in the center of the parent `div` by using the `flex` properties on its styling.

The former allows for better testing.

# Bug 3: Cannot select _All Employees_ after selecting an employee

We handle a case where the new value has the same `ID` as our `EMPTY_EMPLOYEE` – in this case, we load all transactions.

# Bug 4: Clicking on View More button not showing correct data

The response object of the hook returns the new data appended to the existing data, instead of just the new data. During this I also uncovered a bug where users are able to continue viewing more despite there not being another page of data. In this case, viewing more should not be an option.

# Bug 5: Employees filter not available during loading more data

Use the `loading` property of `employeeUtils` to denote the loading state of that particular dropdown.

# Bug 6: View more button not working as expected

Fixed during Bug 4
