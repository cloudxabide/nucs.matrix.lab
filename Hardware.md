# Hardware


| Hostname | System Manufacturer | Baseboard | Processor             | Procs / Cores | Memory | Single-Core | Multi-Core |
|:--------:|:-------------------:|:---------:|:---------------------:|:-------------:|:------:|:----:|:----:|
| sati     | Intel Corporation   | NUC5i5RYB | Core(TM) i5-5250U CPU | 2 / 4         | 15Gi   | 724  | 1521 |
| morpheus | Intel Corporation   | NUC7i7BNB | Core(TM) i7-7567U CPU | 2 / 4         | 31Gi   | 1134 | 2516 |
| neo      | Intel(R) Client Systems | NUC10i7FNB | Core(TM) i7-10710U CPU | 6 / 12  | 62Gi   | 1117 | 6021 | 
| trinity  | Intel(R) Client Systems | NUC10i7FNB | Core(TM) i7-10710U CPU | 6 / 12  | 62Gi   | 1127 | 6002 |


```
echo "| `hostname -s` | `dmidecode -s baseboard-manufacturer` | `dmidecode -s baseboard-product-name` |`lscpu | grep "^Model name:" | grep -o -P '(?<=Intel\(R\)).*(?=\@)'`|`grep "cpu cores" /proc/cpuinfo | awk -F\: '{ print $2 }' | uniq` / `grep "cpu cores" /proc/cpuinfo 2>/dev/null |wc -l` | `free -h | grep "Mem:" | awk '{ print $2 }'` |"

```

