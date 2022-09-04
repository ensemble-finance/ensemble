# ensemble
Roadmap:

1. General refactoring of lib.rs file
    1. Moving low-level functionality to separate files
    2. Adding a types.rs file and moving some types to the file
    3. Removal of redundant validity checks (e.g. if user has enough funds, … etc)
2. Updating validity checks to new validation system
    1. Move validation logic to separate validation.rs file or folder named validation
        1. A folder would be preferred where it contains a file for each extrinsic validation logic, however there are some validity check common to all so you would have to decide which file should contain it
3. Allow the Pool pallet to be instantiable
4. Update Pool pallet’s math
    1. The math itself can be moved to composable-math or something similar so it can be accessible to all pallets
5. General refactoring of tests.rs file
    1. Creating a tests folder
    2. Create a test for each extrinsic
    3. Move tests helper functionality into a helpers.rs file
    4. Move propcompose functionality into a prop_compose.rs file
6. ~~Move code to new repo~~