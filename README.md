# MorePy
## FAQ
### What is MorePy?
MorePy is a library made to introduce more features to Python, such as a two-dimensional table of contents and a hand-made HashMap class
## Documentation
### ColumnTypes
ColumnTypes is an Enum class, meaning that the following are its usagesL
```py
ColumnTypes.automatic_id # Will return an error if used in a Matrix
ColumnTypes.string
ColumnTypes.integer
ColumnTypes.Real
```
### Column
`Column(name: str, kind: ColumnTypes)` -- Creates a new Columnn
#### Properties
- `Column.name`
- `Column.kind` (equivilant to `Column.type`)
### Matrix
!!  The `Matrix` class is still under work and is not recommended for production. You should use the built-in dictionaries instead!
`Matrix(*columns: Column)` -- Creates a new Matrix
`add_column(*columns: Column)` -- Adds a new column
`add_row(**data)` -- Adds a new row. You need to parse as arguments values for each column you defined in the table
### HashMap
The `HashMap` class should just be initialized with a dictionary or two lists, and behaves similarly to a normal dictionary. We would recommend using the built-in `dict` instead, as the `HashMap` class still has bugs.
### ErrorSuppressor
The `ErrorSuppressor` class is made to be used as a context manager.
Syntax: `ErrorSuppressor(errors: tuple[Exception] = ())`
### sum_of_array(array: np.ndarray)
Returns the sum of all items in an array
### sum_of_arange(arange: np.arange)
Self-Explanatory
### sum_of_range(Range: range)
Self-Explanatory
### execute(command: str)
Execute a console command. (Command behavior may differ based on the operating system)
Is equivalent to doing `os.sys()`
Can also be used as `execute(*commands: str)` to run multiple consecutive commands