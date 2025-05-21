import math
import time
from datetime import datetime


class Customer:
    def __init__(self, name, email, _id):
        print('New Customer')
        self.name = name
        self.email = email
        self._id = _id

    @property
    def id(self):
        return self._id

    @id.setter
    def id(self, value):
        if value >= 0:
            self._id = value

    def __str__(self):
        return f"Customer('name={self.name}', 'email={self.email}', 'id={self._id}')"

    def __repr__(self):
        return f"Customer('name={self.name}', 'email={self.email}', 'id={self._id}')"


c1 = Customer("Alice", "alice@example.com", 101)
c2 = Customer("Bob", "bob@example.com", 202)

c1.id = -5

print(c1)
print(repr(c2))
