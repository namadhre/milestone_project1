# milestone_project1
MENU_PROMPT = "\nEnter 'a' to add a movie, 'l' to see your movies, 'f' to find a movie by title, or 'q' to quit: "
movies = []


def add_movie():
    title = input("Enter the movie title: ")
    director = input("Enter the movie director: ")
    year = input("Enter the movie release year: ")

    movies.append({
        'title': title,
        'director': director,
        'year': year
    })


def list_movies():
    for movie in movies:
        print(movie)


def find_movies():
    detail=input("Enter what you want :")
    for movie in movies:
        if movie['title']==detail:
            print(movie)
            break


# And another function here for the user menu
def user_menu():
    selection = input(MENU_PROMPT)
    while selection != 'q':
        if selection == "a":
            add_movie()
            pass
        elif selection == "l":
            list_movies()
            pass
        elif selection == "f":
            find_movies()
            pass
        else:
            print('Unknown command. Please try again.')

        selection = input(MENU_PROMPT)


user_menu()
