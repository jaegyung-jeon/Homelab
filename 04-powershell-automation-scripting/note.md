for loop vs while loop
>>depending on condituions failure. if want to stop when the moment of conditions failing, go to while.
>>>>for loop : for ($i= ; $i -condtion; $i++/--) {
    Write-Host "blahblahblah"
}

>>>>while loop : $i= declaire
>>>>             while($i -condition) {
                    Write-host ""
                    $i++/--
                    }

for each : looping among the list
>>>foreach loop : $list = @('a', 'b', 'c') 
                  foreach ($individual in $list) {
                    write-host "list:$individual"
                  }

function
>funciton name {
    param (
        [int]$a,
        [int]$b
    )
    return $a + $b

}
$result = name -a number -b number
write-host "result:$result"

### pipelines
>- Where-Object : filtering data
>- Sort-Object  : arranging data
>- Select-Object: reshaping data
>- Export-Csv   : exporting data to csv file


