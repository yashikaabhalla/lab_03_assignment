class FlightTable:
    def _init_(self):
        self.table = [
            {"Location": "Mumbai", "Team 01": "India", "Team 02": "Sri Lanka", "Timing": "DAY"},
            {"Location": "Delhi", "Team 01": "England", "Team 02": "Australia", "Timing": "DAY-NIGHT"},
            {"Location": "Chennai", "Team 01": "India", "Team 02": "South Africa", "Timing": "DAY"},
            {"Location": "Indore", "Team 01": "England", "Team 02": "Sri Lanka", "Timing": "DAY-NIGHT"},
            {"Location": "Mohali", "Team 01": "Australia", "Team 02": "South Africa", "Timing": "DAY-NIGHT"},
            {"Location": "Delhi", "Team 01": "India", "Team 02": "Australia", "Timing": "DAY"}
        ]

    def search_by_team(self, team):
        matches = [match for match in self.table if match["Team 01"] == team or match["Team 02"] == team]
        return matches

    def search_by_location(self, location):
        matches = [match for match in self.table if match["Location"] == location]
        return matches

    def search_by_timing(self, timing):
        matches = [match for match in self.table if match["Timing"] == timing]
        return matches


flight_table = FlightTable()

# Example usage
search_option = int(input("Choose a search parameter:\n1. List of all the matches of a Team\n2. List of Matches on a Location\n3. List of Matches based on timing\n"))

if search_option == 1:
    team = input("Enter the team name: ")
    result = flight_table.search_by_team(team)
elif search_option == 2:
    location = input("Enter the location: ")
    result = flight_table.search_by_location(location)
elif search_option == 3:
    timing = input("Enter the timing: ")
    result = flight_table.search_by_timing(timing)
else:
    print("Invalid search option")

if result:
    print("Search Results:")
    for match in result:
        print(f"Location: {match['Location']}, Team 01: {match['Team 01']}, Team 02: {match['Team 02']}, Timing: {match['Timing']}")
else:
    print("No matches found.")