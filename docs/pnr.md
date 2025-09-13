# Mock PNR Generator

## PNR Format
- Each PNR is **6 characters long**.
- Characters can be **uppercase letters (A-Z)** or **digits (0-9)**.
- Example: `ZX1AB2`, `A9B2C3`.

## Python Pseudo-Code

```python
import random
import string

def gen_pnr():
    chars = string.ascii_uppercase + string.digits
    pnr = ''.join(random.choice(chars) for _ in range(6))
    return pnr

# Example usage
print(gen_pnr())  # Output might be: ZX1AB2
