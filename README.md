# Vertex Capacity Graph

## How to Run the project
`g++ -o proj proj.cpp`<br>
`./proj {input_file}`

## Project Details
This project implements Dinic’s algorithm to calculate the maximum flow in a quadrangular graph with vertex capacities and super sources, to solve addressing a conceptual optimization problem.

### The Problem
Given the constraints imposed by the COVID-19 pandemic, it's essential to determine how many residents of a city can safely visit supermarkets without crossing paths. The city under consideration has a square layout, with streets aligned straight from East to West and from North to South, forming a regular grid pattern.

### Solution Interpretation
This scenario can be represented as a quadrangular graph with vertex capacities, where intersections act as vertices with limited capacities, and streets serve as edges. The problem involves calculating the maximum flow from a super source (representing the residents' locations) to a super target (representing the supermarkets), thereby identifying the highest number of residents that can simultaneously reach supermarkets without intersecting paths.

The solution employs Dinic's algorithm for computing this maximum flow, directly corresponding to the maximum number of residents who can safely access supermarkets under the given constraints.

## Input File Structure

The input file contains information about the number of streets and avenues, as well as the number and locations of citizens and supermarkets. The input is structured as follows:

- The first line containing two integers:
    - `M` - the number of avenues
    - `N` - the number of streets
- The second line containing two integers:
    - `S` - the number of supermarkets
    - `C` - the number of citizens
- The next `S` lines each contain two integers describing the locations of supermarkets:
    - Avenue number and street number (intersection coordinates)
- The next `C` lines each contain two integers describing the locations of citizens:
    - Avenue number and street number (intersection coordinates)

Each supermarket or citizen is located precisely at the intersection defined by the given avenue and street numbers.

## Output
The program's output should consist of a single integer indicating the maximum number of citizens who can reach the supermarkets without crossing paths.

## Example

### Input
5 5<br>
7 7<br>
1 1<br>
1 3<br>
2 4<br>
1 2<br>
1 4<br>
3 4<br>
3 5<br>
2 1<br>
2 3<br>
2 2<br>
3 2<br>
2 5<br>
4 4<br>
5 3<br>

### Output
6
