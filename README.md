# Sets-and-Dictionaries
class DataAnalyzer:
    def __init__(self):
        self.my_set = set()
        self.my_dict = {}

    def add_to_set(self, elements):
        self.my_set.update(elements)

    def remove_from_set(self, element):
        self.my_set.discard(element)

    def get_set(self):
        return self.my_set

    def create_dictionary(self, keys, values):
        self.my_dict = dict(zip(keys, values))

    def update_dictionary(self, key, value):
        self.my_dict[key] = value

    def get_dictionary(self):
        return self.my_dict

    def search_dictionary(self, key):
        return key in self.my_dict

    def remove_from_dictionary(self, key):
        if key in self.my_dict:
            del self.my_dict[key]


# Example usage:
if __name__ == "__main__":
    analyzer = DataAnalyzer()
    
    # Adding elements to the set
    analyzer.add_to_set([1, 2, 3, 4])
    print("Set:", analyzer.get_set())

    # Removing an element from the set
    analyzer.remove_from_set(3)
    print("Set after removing 3:", analyzer.get_set())

    # Creating a dictionary
    keys = ['a', 'b', 'c']
    values = [10, 20, 30]
    analyzer.create_dictionary(keys, values)
    print("Dictionary:", analyzer.get_dictionary())

    # Updating the dictionary
    analyzer.update_dictionary('d', 40)
    print("Dictionary after updating:", analyzer.get_dictionary())

    # Searching for a key in the dictionary
    print("Is 'b' present in the dictionary?", analyzer.search_dictionary('b'))

    # Removing a key from the dictionary
    analyzer.remove_from_dictionary('a')
    print("Dictionary after removing 'a':", analyzer.get_dictionary())
