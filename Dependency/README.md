THIS PROJECT IS A REPRODUCIBLE CASE TO THE VSCODE BUG SINCE 1.57.0

IT'S COMPOSED BY 2 PROJECTS

A DEPENDANT - THAT WE ARE WORKING ON
A DEPENDENCY - THAT WE ARE GOING TO LINK AND ALSO WORK ON

HOW TO REPRODUCE THE BUG

1. CREATE A LINK TO THE DEPENDENCY BY EXECUTING THE FOLLOWING ON /Dependency
```
yarn link
```

2. AFTER THAT MAKE A LINK ON THE DEPENDANT PROJECT, BY EXECUTING THE FOLLOWING ON /Dependant
```
yarn link dependency_bug
```

3. NOW IF YOU GO TO /Dependant/index.js AND TRY TO AUTOCOMPLETE THE FUNCTION **doSomething** that comes from the dependency

4. BUG - THE DEPENDENCY IS IMPORTED USING RELATIVE FILEPATH (**../Dependency/soSomething**) INSTEAD OF DEPENDENCY PATH (**dependency_bug/soSomething**)