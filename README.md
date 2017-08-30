# techs-notes
Unclassified daily notes
## CLANG UBSAN
1. UBSAN build for android target
- use SANITIZE_TARGET="address undefined"  build two passes.
- workaround webrtc so built with allow_undefined_symbols=true

- asan+ubsan
mk/go:
add diag(no-sanitize-trap) + ubsan-runtime-lib ldflags of linkage for whole version buid.

2. ubsan in kernel level
https://www.kernel.org/doc/html/v4.10/dev-tools/ubsan.html

## LLVM
1. updateprebuilts toochains of aosp
https://android.googlesource.com/platform/external/clang/+/dev/ToolchainPrebuilts.md
https://android.googlesource.com/platform/external/clang/+/dev/ToolchainPrebuilts.md

2. dev under linux/ubuntu14.04
http://clang.llvm.org/get_started.html

a. git d/l llvm/clang/rt/etc repos
-- git proxy .gitconfig not works properly
-- git corkscrew   --ng
-- git + tsocks    --ng
-- git + openssl rebuild  --pass
d/l from win64
d/l release xz source file.
tar -Jxf xxx.xz
b. .sh update cmake to 3.8.2 //default 2.8.12.2
c. mkdir build && cmake //libcxx should be deleted 
### clang-static analysis
#### clang-tidy
1. dl extra .git repo
2. build from source
3. use clang-tidy
-- ~ -check=-*,google-*
4. extend new checkers
-- dev workflow
-- refs
https://reviews.llvm.org/D31542
http://bbannier.github.io/blog/2015/05/02/Writing-a-basic-clang-static-analysis-check.html
https://www.kdab.com/clang-tidy-part-1-modernize-source-code-using-c11c14/
http://clang.llvm.org/extra/clang-tidy/
http://clang-developers.42468.n3.nabble.com/advice-with-development-on-clang-tidy-matchers-td4044012.html

#### clang-SA
#### clang warnings

## AI

## BIG DATA

## LINUX BASICS
1. check ram size
dmide -t memory
2. make subst vs sh sed 'sxxxx' 
subst from,to,xxx
3. git proxy set
apt-get purge git/-i git/dpkg -i gitxxx.deb
apt proxy 
4. >.bash_history && history -c
5. auto mount dev -/tec/fstab
6. git clone issues
git http proxy fail caused by gnutls -9
work around:
https://gist.github.com/KuoE0/6620246
build git with openssl instead
  new issues: gcc 4.9 
7. gcc update under ubuntu 
a. 
https://askubuntu.com/questions/937375/upgrading-to-gcc-4-9-fails
b. fix gpg error
https://askubuntu.com/questions/13065/how-do-i-fix-the-gpg-error-no-pubkey



