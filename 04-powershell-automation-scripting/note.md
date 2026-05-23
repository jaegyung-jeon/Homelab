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
