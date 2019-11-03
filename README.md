# target-binaries
target binaries for csi-afl

# fuzz binaries

binutils/readelf:
`afl-fuzz -i seed_dir -o out_dir -t 500 -Q -- ./binutils-2.30/binutils/readelf -a @@`

cjson/cjson:
`afl-fuzz -i seed_dir -o out_dir -x json.dict -t 500 -Q -- ./cjson-1.7.7/fuzzing/cjson @@`

libjpeg/djpeg:
`afl-fuzz -i seed_dir -o out_dir -t 500 -Q -- ./jpeg-9c/djpeg @@`

tcpdump/tcpdump:
`afl-fuzz-saveinputs -i seed_dir -o out_dir -t 500 -Q -- ./tcpdump-4.9.2/tcpdump -nr @@`

lava/base64:
`afl-fuzz -i seed_dir -o out_dir -t 500 -Q -- ./lava_bins/base64 -d @@`

lava/md5sum:
`afl-fuzz -i seed_dir -o out_dir -t 500 -Q -- ./lava_bins/md5sum @@`

lava/uniq:
`afl-fuzz -i seed_dir -o out_dir -t 500 -Q -- ./lava_bins/uniq`

lava/who:
`afl-fuzz -i seed_dir -o out_dir -t 500 -Q -- ./lava_bins/who @@`
