# Bash

#### For with index
```bash
n=3
for ((i = 0; i < $n; i++)); do
    echo $i
done
```

#### For in list
```bash
list=(0 1 2)
for i in "${list[@]}"; do
    echo $i
done
```

#### For in list with `seq`
```bash
list=($(seq 1 2 12))
for i in "${list[@]}"; do
    echo $i
done
```


#### Get path up to the script file
```bash
script_dir=$(dirname "$0")
```
