class Match:
    def __init__(self, location, team1, team2, timing):
        self.location = location
        self.team1 = team1
        self.team2 = team2
        self.timing = timing

class FlightTable:
    def __init__(self):
        self.matches = []

    def add_match(self, match):
        self.matches.append(match)

    def search_by_team(self, team_name):
        return [match for match in self.matches if team_name in [match.team1, match.team2]]

    def search_by_location(self, location):
        return [match for match in self.matches if match.location == location]

    def search_by_timing(self, timing):
        return [match for match in self.matches if match.timing == timing]

def get_input(prompt):
    return input(prompt)

def display_matches(matches):
    for match in matches:
        print(match.location, match.team1, "vs", match.team2, match.timing)

def main():
    table = FlightTable()

    # Adding matches to the table
    table.add_match(Match("Mumbai", "India", "Sri Lanka", "DAY"))
    table.add_match(Match("Delhi", "England", "Australia", "DAY-NIGHT"))
    table.add_match(Match("Chennai", "India", "South Africa", "DAY"))
    table.add_match(Match("Indore", "England", "Sri Lanka", "DAY-NIGHT"))
    table.add_match(Match("Mohali", "Australia", "South Africa", "DAY-NIGHT"))
    table.add_match(Match("Delhi", "India", "Australia", "DAY"))

    while True:
        print("\nSearch options:")
        print("1. List of all matches of a Team")
        print("2. List of Matches on a Location")
        print("3. List of Matches based on timing")
        print("4. Exit")
        choice = int(get_input("Enter your choice: "))

        if choice == 1:
            team_name = get_input("Enter the team name: ")
            team_matches = table.search_by_team(team_name)
            print("\nMatches involving", team_name)
            display_matches(team_matches)

        elif choice == 2:
            location = get_input("Enter the location: ")
            location_matches = table.search_by_location(location)
            print("\nMatches at", location)
            display_matches(location_matches)

        elif choice == 3:
            timing = get_input("Enter the timing: ")
            timing_matches = table.search_by_timing(timing)
            print("\nMatches with timing", timing)
            display_matches(timing_matches)

        elif choice == 4:
            break

if __name__ == "__main__":
    main()
