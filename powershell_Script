function get-firstrecurringcharacter {
   [CmdletBinding()]
   param (
     [string]$abcdedcba
   )
  $a = [ordered]@{}
  $b = [ordered]@{}
  $abcdedcba.ToLower().ToCharArray() |
   foreach {
     if ($a.$psitem) {
        $a.$psitem += 1
        if(!$b.$psitem){
        $b += @{$psitem = 1}
     }
        
     }
     else {
       $a += @{$psitem = 1}
     }

  }

  $b.GetEnumerator() |  select -First 1

}
$ts = 'abcdedcba'

get-firstrecurringcharacter -abcdedcba $ts
