# Automaton Analysis and Zielonka’s Algorithm Implementation


Overview

This project is focused on analyzing an HOA (High-level Automaton) file using the Spot library and implementing Zielonka’s algorithm for solving parity games. The script reads an HOA file, extracts controllable atomic propositions (APs), and applies Zielonka’s algorithm to determine the winning regions and strategies for both players based on the automaton’s priorities.

Requirements

	•	Python 3.x
	•	Spot library: Install it using pip install spot (or follow Spot’s installation instructions if needed).
	•	A file containing the automaton in HOA format (e.g., .gm.bz2.ehoa).

File Structure

	•	parse_controllable_ap.py: Contains functions for parsing controllable APs from the HOA file.
	•	zielonka_algorithm.py: Implements Zielonka’s algorithm for solving parity games using the automaton’s state transitions and priorities.
	•	main.py: The main script that loads the HOA file, processes the automaton, and runs the algorithm.

How It Works

	1.	Parsing Controllable APs: The script extracts the controllable APs from the HOA file, which define the atomic propositions relevant to the automaton.
	2.	Loading Automaton: The HOA file is read and the automaton is loaded using the Spot library. The script assumes that the file contains a single automaton.
	3.	Zielonka’s Algorithm:
	•	The script applies Zielonka’s algorithm to solve a parity game. The algorithm is based on alternating between two players (Player 0 with even priorities and Player 1 with odd priorities) and determining their dominion in the automaton.
	•	The winning region and strategy for both players are calculated based on the automaton’s state transitions and the priorities of the states.
	4.	Output:
	•	The automaton’s properties (number of states, initial state, atomic propositions) are displayed.
	•	The algorithm prints the winning regions for each state and the strategy that guarantees a win for each player.
