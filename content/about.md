# About Me 👋

```python
from app.exceptions import *

class Me:
    def __init__(self):
        self.name      = "Pascal Prins"
        self.title     = "Platform Solutioneer"
        self.email     = "hello@foobar-it.com"
        self.city      = "Zwartewaal"
        self.country   = "The Netherlands"
        self.status    = "UNAVAILABLE"

    def is_available(self) -> bool:
        return self.status == "AVAILABLE"

    def request(self) -> str:
        if self.is_available():
            return f"🥳 Yes, I'm available! Let's talk! Reach me at {self.email}"
                
        else:
            throw NotAvailableException(f"{self.name} is not available right now")

```