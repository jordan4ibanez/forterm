# forterm

Standardized terminal colorization for Fortran projects.

-----

4 levels:
- Error
- Warning
- Advisory
- Notification
  
-----

If you like what I do, and would like to support me: [My Patreon](https://www.patreon.com/jordan4ibanez)

-----

## Example:

```fortran
program example
  use, intrinsic :: iso_c_binding
  use :: forterm
  implicit none

  character(len = :, kind = c_char), allocatable :: text

  ! I don't think this really needs any explanation.

  call print_color(ERROR, "This is an error.")
  call print_color(WARNING, "This is a warning.")
  call print_color(ADVISORY, "This is an advisory.")
  call print_color(NOTIFICATION, "This is a notification.")

  text = color_term(NOTIFICATION, "example text")

  print*,text

end program example
```