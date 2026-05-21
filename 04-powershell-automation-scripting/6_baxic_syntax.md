# PowerShell Basic Tutorial for Beginners

This tutorial covers the basic building blocks of PowerShell from scratch.
It includes: Variables, If/Else, Loops, Functions, Pipelines, and Objects.

---

## 1. Variables

Variables store values you can use later.

- Start with `$`
- No need to declare a type in most cases

Example:

```powershell
$greeting = "Hello, PowerShell!"
$number = 10
$isReady = $true

Write-Host $greeting
Write-Host "Number is $number"
Write-Host "Ready? $isReady"
```

PowerShell can also use typed variables:

```powershell
[int]$count = 5
[string]$name = "Alice"
```

Use `Get-Variable` to see variables and `Remove-Variable` to delete them:

```powershell
Get-Variable
Remove-Variable -Name greeting
```

---

## 2. If / Else

Use `if`, `elseif`, and `else` to make decisions.

```powershell
$age = 18

if ($age -ge 18) {
    Write-Host "You are an adult."
} elseif ($age -ge 13) {
    Write-Host "You are a teenager."
} else {
    Write-Host "You are a child."
}
```

Common comparison operators:

- `-eq` equals
- `-ne` not equals
- `-gt` greater than
- `-lt` less than
- `-ge` greater than or equal
- `-le` less than or equal
- `-like` wildcard match
- `-match` regex match

Example with string comparison:

```powershell
$name = "bob"

if ($name -eq "bob") {
    Write-Host "Hello Bob"
} else {
    Write-Host "Who are you?"
}
```

---

## 3. Loops

Loops repeat code until a condition changes.

### `for` loop

```powershell
for ($i = 1; $i -le 5; $i++) {
    Write-Host "Count: $i"
}
```

### `while` loop

```powershell
$count = 1
while ($count -le 5) {
    Write-Host "While count: $count"
    $count++
}
```

### `foreach` loop

Great for iterating over lists and arrays.

```powershell
$fruits = @('Apple', 'Banana', 'Cherry')
foreach ($fruit in $fruits) {
    Write-Host "Fruit: $fruit"
}
```

---

## 4. Functions

Functions let you package reusable logic.

```powershell
function Say-Hello {
    param (
        [string]$Name = 'User'
    )

    Write-Host "Hello, $Name!"
}

Say-Hello -Name "Sam"
```

Functions can return values:

```powershell
function Add-Numbers {
    param (
        [int]$a,
        [int]$b
    )
    return $a + $b
}

$result = Add-Numbers -a 3 -b 4
Write-Host "Result: $result"
```

Use `Get-Help` for functions:

```powershell
Get-Help About_Functions
```

---

## 5. Pipelines

Pipelines let you pass output from one command into another.

```powershell
Get-Process | Where-Object {$_.CPU -gt 1} | Sort-Object CPU -Descending
```

Example with simple objects:

```powershell
1..5 | ForEach-Object { $_ * 2 }
```

Another example:

```powershell
Get-Service | Where-Object {$_.Status -eq 'Running'} | Select-Object Name, Status
```

Common pipeline cmdlets:

- `Where-Object` to filter
- `Select-Object` to choose properties
- `Sort-Object` to order results
- `ForEach-Object` to run code for every item

---

## 6. Objects

PowerShell works with objects, not plain text.

Example:

```powershell
$process = Get-Process -Name notepad
Write-Host $process.Name
Write-Host $process.Id
Write-Host $process.WorkingSet
```

Use `Get-Member` to inspect object properties and methods:

```powershell
Get-Process | Get-Member
```

Objects can have custom properties:

```powershell
$computer = [PSCustomObject]@{
    Name = 'SERVER01'
    IP = '192.168.1.10'
    Online = $true
}

$computer | Format-Table
```

---

## Getting Started

1. Open PowerShell.
2. Type commands directly and press Enter.
3. Save scripts in a `.ps1` file.
4. Run scripts with `.ilename.ps1`.
5. If needed, set the execution policy temporarily:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

---

## Quick Practice

Try these steps:

- Create a variable and print it.
- Write an `if` statement that checks a number.
- Loop through an array with `foreach`.
- Write a simple function that returns a value.
- Use a pipeline to filter a command output.
- Inspect an object with `Get-Member`.

Good luck! This gives you the six core PowerShell basics to build from scratch.
