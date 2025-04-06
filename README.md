
phones = {}
books = {}
movies = {}
watches = {}
cars = {}


def add_phone(phones):
    name = input("Podaj nazwę telefonu: ")
    mark = input("Jakiej firmy jest telefon: ")
    year = input("Podaj rok wydania: ")
    ram = input("Podaj ile ma ramu: ")
    storage = input("Podaj ile ma pamięci: ")

    phone = {
        "name": name,
        "mark": mark,
        "ram": int(ram),
        "year": int(year),
        "storage": int(storage)
    }
    phones[name.lower()] = phone
    print(f'Telefon "{name}" został dodany.')

def remove_phone(phones):
    name = input("Podaj tytuł telefonu do usunięcia: ")
    if name.lower() in phones:
        del phones[name.lower()]
        print(f'Telefon "{name}" został usunięty.')
    else:
        print(f'Nie znaleziono telefonu "{name}".')

def edit_phone(phones):
    name = input("Podaj tytuł telefonu do edycji: ")
    if name.lower() in phones:
        phone = phones[name.lower()]
        new_name = input(f"Nowa nazwa ({phone['name']}): ")
        new_mark = input(f"Nowa marka ({phone['mark']}): ")
        new_year = input(f"Nowy rok wydania ({phone['year']}): ")
        new_ram = input(f"Nowy ram ({phone['ram']}): ")
        new_storage = input(f"Nowa pamięć ({phone['storage']}): ")

        phone["name"] = new_name if new_name else phone["name"]
        phone["mark"] = new_mark if new_mark else phone["mark"]
        phone["year"] = int(new_year) if new_year else phone["year"]
        phone["ram"] = int(new_ram) if new_ram else phone["ram"]
        phone["storage"] = int(new_storage) if new_storage else phone["storage"]
        print(f'Telefon "{name}" został zaktualizowany.')
    else:
        print(f'Nie znaleziono telefonu "{name}".')

def show_phones(phones):
    if not phones:
        print("Brak telefonów w bibliotece.")
    else:
        print("\nLista telefonów:")
        for phone in phones.values():
            print(f'{phone["name"]} - {phone["mark"]} ({phone["year"]}) - {phone["ram"]} GB, {phone["storage"]} GB')


def add_book(books):
    title = input("Podaj tytuł książki: ")
    author = input("Podaj autora książki: ")
    year = input("Podaj rok wydania: ")
    genre = input("Podaj gatunek książki: ")
    pages = input("Podaj liczbę stron: ")

    book = {
        "title": title,
        "author": author,
        "year": int(year),
        "genre": genre,
        "pages": int(pages)
    }
    books[title.lower()] = book
    print(f'Książka "{title}" została dodana.')

def remove_book(books):
    title = input("Podaj tytuł książki do usunięcia: ")
    if title.lower() in books:
        del books[title.lower()]
        print(f'Książka "{title}" została usunięta.')
    else:
        print(f'Nie znaleziono książki "{title}".')

def edit_book(books):
    title = input("Podaj tytuł książki do edycji: ")
    if title.lower() in books:
        book = books[title.lower()]
        new_title = input(f"Nowy tytuł ({book['title']}): ")
        new_author = input(f"Nowy autor ({book['author']}): ")
        new_year = input(f"Nowy rok wydania ({book['year']}): ")
        new_genre = input(f"Nowy gatunek ({book['genre']}): ")
        new_pages = input(f"Nowa liczba stron ({book['pages']}): ")

        book["title"] = new_title if new_title else book["title"]
        book["author"] = new_author if new_author else book["author"]
        book["year"] = int(new_year) if new_year else book["year"]
        book["genre"] = new_genre if new_genre else book["genre"]
        book["pages"] = int(new_pages) if new_pages else book["pages"]
        print(f'Książka "{title}" została zaktualizowana.')
    else:
        print(f'Nie znaleziono książki "{title}".')

def show_books(books):
    if not books:
        print("Brak książek w bibliotece.")
    else:
        print("\nLista książek:")
        for book in books.values():
            print(f'{book["title"]} - {book["author"]} ({book["year"]}) - {book["genre"]}, {book["pages"]} stron')


def add_movie(movies):
    title = input("Podaj tytuł filmu: ")
    director = input("Podaj reżysera filmu: ")
    year = input("Podaj rok wydania: ")
    genre = input("Podaj gatunek filmu: ")
    duration = input("Podaj czas trwania (w minutach): ")

    movie = {
        "title": title,
        "director": director,
        "year": int(year),
        "genre": genre,
        "duration": int(duration)
    }
    movies[title.lower()] = movie
    print(f'Film "{title}" został dodany.')

def remove_movie(movies):
    title = input("Podaj tytuł filmu do usunięcia: ")
    if title.lower() in movies:
        del movies[title.lower()]
        print(f'Film "{title}" został usunięty.')
    else:
        print(f'Nie znaleziono filmu "{title}".')

def edit_movie(movies):
    title = input("Podaj tytuł filmu do edycji: ")
    if title.lower() in movies:
        movie = movies[title.lower()]
        new_title = input(f"Nowy tytuł ({movie['title']}): ")
        new_director = input(f"Nowy reżyser ({movie['director']}): ")
        new_year = input(f"Nowy rok wydania ({movie['year']}): ")
        new_genre = input(f"Nowy gatunek ({movie['genre']}): ")
        new_duration = input(f"Nowy czas trwania ({movie['duration']}): ")

        movie["title"] = new_title if new_title else movie["title"]
        movie["director"] = new_director if new_director else movie["director"]
        movie["year"] = int(new_year) if new_year else movie["year"]
        movie["genre"] = new_genre if new_genre else movie["genre"]
        movie["duration"] = int(new_duration) if new_duration else movie["duration"]
        print(f'Film "{title}" został zaktualizowany.')
    else:
        print(f'Nie znaleziono filmu "{title}".')

def show_movies(movies):
    if not movies:
        print("Brak filmów w bibliotece.")
    else:
        print("\nLista filmów:")
        for movie in movies.values():
            print(f'{movie["title"]} - {movie["director"]} ({movie["year"]}) - {movie["genre"]}, {movie["duration"]} min')


def add_watch(watches):
    name = input("Podaj nazwę zegarka: ")
    brand = input("Podaj markę zegarka: ")
    year = input("Podaj rok wydania: ")
    type_watch = input("Podaj typ zegarka: ")
    price = input("Podaj cenę zegarka: ")

    watch = {
        "name": name,
        "brand": brand,
        "year": int(year),
        "type": type_watch,
        "price": float(price)
    }
    watches[name.lower()] = watch
    print(f'Zegarek "{name}" został dodany.')

def remove_watch(watches):
    name = input("Podaj nazwę zegarka do usunięcia: ")
    if name.lower() in watches:
        del watches[name.lower()]
        print(f'Zegarek "{name}" został usunięty.')
    else:
        print(f'Nie znaleziono zegarka "{name}".')

def edit_watch(watches):
    name = input("Podaj nazwę zegarka do edycji: ")
    if name.lower() in watches:
        watch = watches[name.lower()]
        new_name = input(f"Nowa nazwa ({watch['name']}): ")
        new_brand = input(f"Nowa marka ({watch['brand']}): ")
        new_year = input(f"Nowy rok wydania ({watch['year']}): ")
        new_type = input(f"Nowy typ ({watch['type']}): ")
        new_price = input(f"Nowa cena ({watch['price']}): ")

        watch["name"] = new_name if new_name else watch["name"]
        watch["brand"] = new_brand if new_brand else watch["brand"]
        watch["year"] = int(new_year) if new_year else watch["year"]
        watch["type"] = new_type if new_type else watch["type"]
        watch["price"] = float(new_price) if new_price else watch["price"]
        print(f'Zegarek "{name}" został zaktualizowany.')
    else:
        print(f'Nie znaleziono zegarka "{name}".')

def show_watches(watches):
    if not watches:
        print("Brak zegarków w bibliotece.")
    else:
        print("\nLista zegarków:")
        for watch in watches.values():
            print(f'{watch["name"]} - {watch["brand"]} ({watch["year"]}) - {watch["type"]}, {watch["price"]} zł')


def add_car(cars):
    model = input("Podaj model samochodu: ")
    brand = input("Podaj markę samochodu: ")
    year = input("Podaj rok produkcji: ")
    engine = input("Podaj pojemność silnika: ")
    price = input("Podaj cenę samochodu: ")

    car = {
        "model": model,
        "brand": brand,
        "year": int(year),
        "engine": engine,
        "price": float(price)
    }
    cars[model.lower()] = car
    print(f'Samochód "{model}" został dodany.')

def remove_car(cars):
    model = input("Podaj model samochodu do usunięcia: ")
    if model.lower() in cars:
        del cars[model.lower()]
        print(f'Samochód "{model}" został usunięty.')
    else:
        print(f'Nie znaleziono samochodu "{model}".')

def edit_car(cars):
    model = input("Podaj model samochodu do edycji: ")
    if model.lower() in cars:
        car = cars[model.lower()]
        new_model = input(f"Nowy model ({car['model']}): ")
        new_brand = input(f"Nowa marka ({car['brand']}): ")
        new_year = input(f"Nowy rok produkcji ({car['year']}): ")
        new_engine = input(f"Nowa pojemność silnika ({car['engine']}): ")
        new_price = input(f"Nowa cena ({car['price']}): ")

        car["model"] = new_model if new_model else car["model"]
        car["brand"] = new_brand if new_brand else car["brand"]
        car["year"] = int(new_year) if new_year else car["year"]
        car["engine"] = new_engine if new_engine else car["engine"]
        car["price"] = float(new_price) if new_price else car["price"]
        print(f'Samochód "{model}" został zaktualizowany.')
    else:
        print(f'Nie znaleziono samochodu "{model}".')

def show_cars(cars):
    if not cars:
        print("Brak samochodów w bibliotece.")
    else:
        print("\nLista samochodów:")
        for car in cars.values():
            print(f'{car["model"]} - {car["brand"]} ({car["year"]}) - {car["engine"]}, {car["price"]} zł')


def book_menu(books):
    while True:
        print("\n--- Biblioteka Książek ---")
        print("1. Dodaj książkę")
        print("2. Usuń książkę")
        print("3. Edytuj książkę")
        print("4. Pokaż książki")
        print("0. Powrót")
        choice = input("Wybierz opcję: ")

        if choice == "1":
            add_book(books)
        elif choice == "2":
            remove_book(books)
        elif choice == "3":
            edit_book(books)
        elif choice == "4":
            show_books(books)
        elif choice == "0":
            break
        else:
            print("Nieprawidłowy wybór.")

def phone_menu(phones):
    while True:
        print("\n--- Biblioteka Telefonów ---")
        print("1. Dodaj telefon")
        print("2. Usuń telefon")
        print("3. Edytuj telefon")
        print("4. Pokaż telefony")
        print("0. Powrót")
        choice = input("Wybierz opcję: ")

        if choice == "1":
            add_phone(phones)
        elif choice == "2":
            remove_phone(phones)
        elif choice == "3":
            edit_phone(phones)
        elif choice == "4":
            show_phones(phones)
        elif choice == "0":
            break
        else:
            print("Nieprawidłowy wybór.")

def movie_menu(movies):
    while True:
        print("\n--- Biblioteka Filmów ---")
        print("1. Dodaj film")
        print("2. Usuń film")
        print("3. Edytuj film")
        print("4. Pokaż filmy")
        print("0. Powrót")
        choice = input("Wybierz opcję: ")

        if choice == "1":
            add_movie(movies)
        elif choice == "2":
            remove_movie(movies)
        elif choice == "3":
            edit_movie(movies)
        elif choice == "4":
            show_movies(movies)
        elif choice == "0":
            break
        else:
            print("Nieprawidłowy wybór.")

def watch_menu(watches):
    while True:
        print("\n--- Biblioteka Zegarków ---")
        print("1. Dodaj zegarek")
        print("2. Usuń zegarek")
        print("3. Edytuj zegarek")
        print("4. Pokaż zegarki")
        print("0. Powrót")
        choice = input("Wybierz opcję: ")

        if choice == "1":
            add_watch(watches)
        elif choice == "2":
            remove_watch(watches)
        elif choice == "3":
            edit_watch(watches)
        elif choice == "4":
            show_watches(watches)
        elif choice == "0":
            break
        else:
            print("Nieprawidłowy wybór.")

def car_menu(cars):
    while True:
        print("\n--- Biblioteka Samochodów ---")
        print("1. Dodaj samochód")
        print("2. Usuń samochód")
        print("3. Edytuj samochód")
        print("4. Pokaż samochody")
        print("0. Powrót")
        choice = input("Wybierz opcję: ")

        if choice == "1":
            add_car(cars)
        elif choice == "2":
            remove_car(cars)
        elif choice == "3":
            edit_car(cars)
        elif choice == "4":
            show_cars(cars)
        elif choice == "0":
            break
        else:
            print("Nieprawidłowy wybór.")


def main_menu():
    while True:
        print("=== MENU GŁÓWNE ===")
        print("1. Biblioteka książek")
        print("2. Biblioteka telefonów")
        print("3. Biblioteka filmów")
        print("4. Biblioteka zegarków")
        print("5. Biblioteka samochodów")
        print("0. Wyjście")

        choice = input("Wybierz opcję: ")
        if choice == "1":
            book_menu(books)
        elif choice == "2":
            phone_menu(phones)
        elif choice == "3":
            movie_menu(movies)
        elif choice == "4":
            watch_menu(watches)
        elif choice == "5":
            car_menu(cars)
        elif choice == "0":
            print("Do widzenia!")
            break
        else:
            print("Nieprawidłowy wybór.")


main_menu()
 
