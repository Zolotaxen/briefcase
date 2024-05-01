# briefcase
class Briefcase:
    def __init__(self, color, material, lock_code):
        self.color = color
        self.material = material
        self.lock_code = lock_code
        self.is_locked = True

    def unlock(self, entered_code):
        if entered_code == self.lock_code:
            self.is_locked = False
            print("Briefcase unlocked.")
        else:
            print("Incorrect code. Briefcase remains locked.")

    def lock(self):
        self.is_locked = True
        print("Briefcase locked.")

# Example usage
if __name__ == "__main__":
    # Creating an instance of the Briefcase class
    my_briefcase = Briefcase(color="Black", material="Leather", lock_code="1234")

    # Attempting to unlock with the wrong code
    my_briefcase.unlock("4321")

    # Attempting to unlock with the correct code
    my_briefcase.unlock("1234")

    # Locking the briefcase
    my_briefcase.lock()
