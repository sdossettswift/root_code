# ROOT Insurance Code Sample

## Approach To Solving Problem
1. The first step in my problem solving is to set up the git repository. I am including the problem statement along with a general outline for the README. I restate the deliverables and specifications to ensure I have a full grasp of the task at hand, and use the README as a path forward.

## Testing

# Deliverables
## Submission
- via tarball or vit bundle
- `GIT_DIR=your-code-dir/.git git bundle create your-code.gitbundle --all`

## Code Specs
- Code to process input file
- Each line of input file begins w/ command
  - Driver Drivername
  - Trip Drivername start end miles
- If Driver
  - create driver in app
- If Trip
  - assign trip to driver, track total miles, track average speed
  - validations:
    - Ignore
      - speed < 5mph
      - speed > 100mph
- Report
  - Each driver, total miles, average speed
  - Sorted:
    - most miles -> fewest miles driven
  - Round
    - miles driven -> integer
    - mph -> integer
