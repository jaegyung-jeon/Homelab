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
>- Get-Service/Process
>- Where-Object : filtering data <filtering by condition, ex:)Where-Object CPU -gt 100>
>- Sort-Object  : arranging data
>- Select-Object: reshaping data
>- Export-Csv   : exporting data to csv file

#### properties
- get-service   : status, name
- get-process   : cpu, name, id
- get-eventlog  : entrytype, message
- get-childitem : name, length, lastwritetime 

### Object

- $process = Get-Process notepad
>>$process.Name = notepad </br>
>>$process.IP   = 192.168.2.4


- $process = [PSCustomObject]@{</br>
    Name = "pc01"</br>
    IP   = "192.168.2.5"</br>
    ONLINE = $true</br>
}

>>$process.Name = pc01</br>
>>$process.IP   = 192.168.2.5</br>
>>$process.ONLINE = true