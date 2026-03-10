# Application-level-Linkedlist-program-9

# Linked List Program - Music Playlist

class Node:
    def __init__(self, song):
        self.song = song
        self.next = None


class LinkedList:
    def __init__(self):
        self.head = None

    def add_song(self, song):
        new_node = Node(song)

        if self.head is None:
            self.head = new_node
            return

        temp = self.head
        while temp.next:
            temp = temp.next

        temp.next = new_node

    def display(self):
        temp = self.head
        while temp:
            print(temp.song)
            temp = temp.next


# Application Example
playlist = LinkedList()

playlist.add_song("Song1")
playlist.add_song("Song2")
playlist.add_song("Song3")

print("Music Playlist:")
playlist.display()




Music Playlist:
Song1
Song2
Song3
