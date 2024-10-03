# basketballimport random
import time

# Teams
team_1 = "Team A"
team_2 = "Team B"

# Initialize scores
score_team_1 = 0
score_team_2 = 0

# Define the quarters and scoring range
quarters = 4
min_points_per_quarter = 15
max_points_per_quarter = 35

def simulate_game():
    global score_team_1, score_team_2
    
    print(f"Tip-off! {team_1} vs {team_2}")
    
    for quarter in range(1, quarters + 1):
        # Random points for each team per quarter
        points_team_1 = random.randint(min_points_per_quarter, max_points_per_quarter)
        points_team_2 = random.randint(min_points_per_quarter, max_points_per_quarter)
        
        score_team_1 += points_team_1
        score_team_2 += points_team_2
        
        # Display score after each quarter
        print(f"End of Quarter {quarter}:")
        print(f"{team_1} scored {points_team_1} points this quarter. Total: {score_team_1}")
        print(f"{team_2} scored {points_team_2} points this quarter. Total: {score_team_2}")
        
        # Simulate time between quarters
        time.sleep(1)
    
    # End of game
    print(f"Full-time! Final Score: {team_1} {score_team_1} : {team_2} {score_team_2}")
    if score_team_1 > score_team_2:
        print(f"{team_1} wins!")
    elif score_team_1 < score_team_2:
        print(f"{team_2} wins!")
    else:
        print("It's a tie!")

# Run the simulation
simulate_game()
