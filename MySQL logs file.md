```
Last login: Wed Mar  2 10:22:20 on console
naitiksinghal@Naitiks-MacBook-Air ~ % mysql -uroot 
ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/tmp/mysql.sock' (2)
naitiksinghal@Naitiks-MacBook-Air ~ % mysql.server start
Starting MySQL
 SUCCESS! 
naitiksinghal@Naitiks-MacBook-Air ~ % mysql -uroot      
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 8
Server version: 8.0.28 Homebrew

Copyright (c) 2000, 2022, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> exit;
Bye
naitiksinghal@Naitiks-MacBook-Air ~ % brew update
Updated 1 tap (homebrew/core).
==> New Formulae
aarch64-elf-binutils                  bkt                                   dpp                                   dynaconf                              litani                                rospo                                 uutils-findutils
aarch64-elf-gcc                       cloudflared                           dsq                                   gst-plugins-rs                        quick-lint-js                         trzsz                                 xkcd
==> Updated Formulae
icu4c ✔                       cdk8s                         docker-gen                    git-series                    kertish-dfs                   mplayer                       pgpdump                       rcs                           tmux-mem-cpu-load
mysql ✔                       cereal                        docker-slim                   git-vendor                    lbdb                          msc-generator                 php                           rollup                        tomcat
advancemame                   certbot                       dolt                          gitfs                         lesspipe                      mtools                        php@7.4                       rom-tools                     tomcat@8
amp                           certigo                       dosbox-x                      gitlab-runner                 libaacs                       ncmpcpp                       php@8.0                       rqlite                        tomcat@9
apngasm                       cgif                          driftctl                      gitless                       libcdr                        nerdctl                       phpstan                       salt                          tracker
arcade-learning-environment   chakra                        dune                          gjs                           libgit2                       netlify-cli                   pinboard-notes-backup         sane-backends                 tree-sitter
argo                          checkstyle                    dvc                           glooctl                       libgit2-glib                  newman                        pipgrip                       scummvm                       trino
arx-libertatis                chezmoi                       dwdiff                        gnunet                        libical                       newrelic-cli                  pnpm                          seaweedfs                     twarc
asciidoc                      clickhouse-odbc               easyrpg-player                gnuplot@4                     liblcf                        newrelic-infra-agent          ponyc                         serverless                    typescript
asyncapi                      clojure                       eksctl                        go                            libmonome                     newt                          poppler                       sile                          urweb
atlantis                      cloog                         enkits                        go@1.16                       libmspub                      nghttp2                       poppler-qt5                   siril                         vapor
atlas                         closure-compiler              erlang@23                     gofish                        libnghttp2                    nginx                         postgis                       skaffold                      vault
aws-cdk                       consul                        esbuild                       gojq                          libphonenumber                ngt                           postgresql                    smartmontools                 vault-cli
aws-sdk-cpp                   consul-template               esphome                       gopls                         libpsl                        nnn                           postgresql@10                 snakemake                     vespa-cli
awscli                        convox                        exploitdb                     goredo                        libsoup@2                     node                          postgresql@11                 sqlite-utils                  vim
azcopy                        corral                        faudio                        grace                         libvisio                      node@10                       postgresql@12                 sqlmap                        visp
azure-cli                     couchdb                       fb303                         grafana                       licensefinder                 node@12                       postgresql@13                 sshs                          vite
bandit                        cpl                           fbthrift                      groonga                       link-grammar                  node@14                       proj                          step                          vte3
basis_universal               cpm                           filebeat                      gtk-gnutella                  literate-git                  node@16                       psalm                         stylua                        wangle
boost                         crun                          firebase-cli                  hadoop                        llvm                          nss                           pulumi                        swift                         wasmer
boost@1.76                    cubejs-cli                    fizz                          harfbuzz                      localstack                    nuclei                        pybind11                      syncthing                     watchman
brigade-cli                   cypher-shell                  flarectl                      hasura-cli                    mame                          oci-cli                       pyright                       sysstat                       webpack
brook                         cyral-gimme-db-token          flow                          hcl2json                      mapnik                        oh-my-posh                    qrcp                          tarantool                     whistle
buildpulse-test-reporter      cyrus-sasl                    fluent-bit                    hfstospell                    mariadb                       okteto                        qt                            tctl                          widelands
byobu                         datalad                       flux                          himalaya                      menhir                        opa                           qt-libiodbc                   tectonic                      xcbeautify
cadence                       dbus                          folly                         httpx                         mercurial                     opencv                        qt-mariadb                    teleport                      xkeyboardconfig
caffe                         dependency-check              fortio                        hugo                          metabase                      openrct2                      qt-mysql                      tendermint                    xplr
calceph                       dhall                         freeling                      infracost                     micronaut                     parquet-cli                   qt-percona-server             tepl                          xrootd
calicoctl                     dhall-bash                    gau                           ipython                       minio                         pazpar2                       qt-postgresql                 terraform                     yaz
cargo-c                       dhall-json                    gedit                         jenkins                       minio-mc                      pdf2djvu                      qt-unixodbc                   terragrunt                    yosys
cargo-edit                    dhall-lsp-server              gegl                          julia                         mlt                           pdftoipe                      qt@5                          tesseract                     zbctl
cargo-llvm-lines              dhall-yaml                    geoserver                     juliaup                       mmv                           percona-server                questdb                       texlive                       zebra
cargo-outdated                django-completion             gh                            jump                          mongo-c-driver                percona-xtrabackup            r                             tfsec                         zk
cbmc                          dnsx                          gimme-aws-creds               just                          mongocli                      perkeep                       radare2                       thanos                        znc
ccache                        docker-compose                git-quick-stats               kamel                         mpd                           pev                           rbspy                         tm                            zorba
==> Deleted Formulae
advancemenu                                                                                                                             pdflib-lite

You have 2 outdated formulae installed.
You can upgrade them with brew upgrade
or list them with brew outdated.
naitiksinghal@Naitiks-MacBook-Air ~ % brew upgrade mysql
==> Upgrading 1 outdated package:
mysql 8.0.28 -> 8.0.28_1
==> Downloading https://ghcr.io/v2/homebrew/core/icu4c/manifests/70.1
######################################################################## 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/icu4c/blobs/sha256:43cf787a35559b90597db8e1aaba95dbeedb84b1ee3d2e942be8938ae618724c
==> Downloading from https://pkg-containers.githubusercontent.com/ghcr1/blobs/sha256:43cf787a35559b90597db8e1aaba95dbeedb84b1ee3d2e942be8938ae618724c?se=2022-03-04T19%3A15%3A00Z&sig=7liY%2BRfHKJYPLo3E2Lb4BMj2TrQVeIxkj8YhcIVG0eE%3D&sp=r&spr=https&sr=b&sv=2019-12-12
######################################################################## 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/mysql/manifests/8.0.28_1
######################################################################## 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/mysql/blobs/sha256:c51f67f07e7a419c14d3f2e68cab306b5b618c56ab61bef26abbb6d24986d4ed
==> Downloading from https://pkg-containers.githubusercontent.com/ghcr1/blobs/sha256:c51f67f07e7a419c14d3f2e68cab306b5b618c56ab61bef26abbb6d24986d4ed?se=2022-03-04T19%3A15%3A00Z&sig=%2BjyX1d5dvRRv4qz3jPEhJQU9Fn71uBMLY4O2cRRYAts%3D&sp=r&spr=https&sr=b&sv=2019-12-12
######################################################################## 100.0%
==> Upgrading mysql
  8.0.28 -> 8.0.28_1 

==> Installing dependencies for mysql: icu4c
==> Installing mysql dependency: icu4c
==> Pouring icu4c--70.1.arm64_monterey.bottle.tar.gz
🍺  /opt/homebrew/Cellar/icu4c/70.1: 261 files, 74.9MB
==> Installing mysql
==> Pouring mysql--8.0.28_1.arm64_monterey.bottle.tar.gz
==> Caveats
We've installed your MySQL database without a root password. To secure it run:
    mysql_secure_installation

MySQL is configured to only allow connections from localhost by default

To connect run:
    mysql -uroot

To restart mysql after an upgrade:
  brew services restart mysql
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/mysql/bin/mysqld_safe --datadir=/opt/homebrew/var/mysql
==> Summary
🍺  /opt/homebrew/Cellar/mysql/8.0.28_1: 304 files, 294.3MB
==> Running `brew cleanup mysql`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
Removing: /opt/homebrew/Cellar/mysql/8.0.28... (304 files, 294.3MB)
==> Caveats
==> mysql
We've installed your MySQL database without a root password. To secure it run:
    mysql_secure_installation

MySQL is configured to only allow connections from localhost by default

To connect run:
    mysql -uroot

To restart mysql after an upgrade:
  brew services restart mysql
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/mysql/bin/mysqld_safe --datadir=/opt/homebrew/var/mysql
naitiksinghal@Naitiks-MacBook-Air ~ % mysql -uroot
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.28 Homebrew

Copyright (c) 2000, 2022, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| employee           |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.02 sec)

mysql> use employee;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> show tables;
+--------------------+
| Tables_in_employee |
+--------------------+
| empl               |
+--------------------+
1 row in set (0.00 sec)

mysql> show dataqbases
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'dataqbases' at line 1
mysql> desc employee;
ERROR 1146 (42S02): Table 'employee.employee' doesn't exist
mysql> desc empl;
+----------+-------------+------+-----+---------+-------+
| Field    | Type        | Null | Key | Default | Extra |
+----------+-------------+------+-----+---------+-------+
| empno    | int         | YES  |     | NULL    |       |
| ename    | varchar(20) | YES  |     | NULL    |       |
| job      | varchar(20) | YES  |     | NULL    |       |
| mgr      | int         | YES  |     | NULL    |       |
| hiredate | datetime    | YES  |     | NULL    |       |
| sal      | float       | YES  |     | NULL    |       |
| comm     | int         | YES  |     | NULL    |       |
| deptno   | int         | YES  |     | NULL    |       |
+----------+-------------+------+-----+---------+-------+
8 rows in set (0.00 sec)

mysql> select * from empl;
+-------+-----------+-----------+------+---------------------+------+------+--------+
| empno | ename     | job       | mgr  | hiredate            | sal  | comm | deptno |
+-------+-----------+-----------+------+---------------------+------+------+--------+
|  8499 | ANYA      | SALESMAN  | 8698 | 1991-02-20 00:00:00 | 1600 |  300 |     30 |
|  8521 | SETH      | SALESMAN  | 8698 | 1991-02-22 00:00:00 | 1250 |  500 |     30 |
|  8566 | MAHADEVAN | MANAGER   | 8839 | 1991-04-02 00:00:00 | 2985 | NULL |     20 |
|  8654 | MOMIN     | SALESMAN  | 8698 | 1991-09-28 00:00:00 | 1250 | 1400 |     30 |
|  8698 | MAHADEVAN | MANAGER   | 8839 | 1991-05-01 00:00:00 | 2850 | NULL |     30 |
|  8882 | SHIVANSH  | MANAGER   | 8839 | 1991-06-09 00:00:00 | 2450 | NULL |     10 |
|  8888 | SCOTT     | ANALYST   | 8566 | 1992-12-09 00:00:00 | 3000 | NULL |     20 |
|  8839 | AMIR      | PRESIDENT | NULL | 1991-11-18 00:00:00 | 5000 | NULL |     10 |
|  8844 | KULDEEP   | SALESMAN  | 8698 | 1991-09-08 00:00:00 | 1500 |    0 |     30 |
|  8886 | ANOOP     | CLERK     | 8888 | 1993-01-12 00:00:00 | 1100 | NULL |     20 |
|  8900 | JATIN     | CLERK     | 8698 | 1991-12-03 00:00:00 |  950 | NULL |     30 |
|  8902 | FAKIR     | ANALYST   | 8566 | 1991-12-03 00:00:00 | 3000 | NULL |     20 |
|  8934 | MITA      | CLERK     | 8882 | 1992-01-02 00:00:00 | 1300 | NULL |     10 |
+-------+-----------+-----------+------+---------------------+------+------+--------+
13 rows in set (0.00 sec)

mysql> selct * from empl;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'selct * from empl' at line 1
mysql> select * from empl;
+-------+-----------+-----------+------+---------------------+------+------+--------+
| empno | ename     | job       | mgr  | hiredate            | sal  | comm | deptno |
+-------+-----------+-----------+------+---------------------+------+------+--------+
|  8499 | ANYA      | SALESMAN  | 8698 | 1991-02-20 00:00:00 | 1600 |  300 |     30 |
|  8521 | SETH      | SALESMAN  | 8698 | 1991-02-22 00:00:00 | 1250 |  500 |     30 |
|  8566 | MAHADEVAN | MANAGER   | 8839 | 1991-04-02 00:00:00 | 2985 | NULL |     20 |
|  8654 | MOMIN     | SALESMAN  | 8698 | 1991-09-28 00:00:00 | 1250 | 1400 |     30 |
|  8698 | MAHADEVAN | MANAGER   | 8839 | 1991-05-01 00:00:00 | 2850 | NULL |     30 |
|  8882 | SHIVANSH  | MANAGER   | 8839 | 1991-06-09 00:00:00 | 2450 | NULL |     10 |
|  8888 | SCOTT     | ANALYST   | 8566 | 1992-12-09 00:00:00 | 3000 | NULL |     20 |
|  8839 | AMIR      | PRESIDENT | NULL | 1991-11-18 00:00:00 | 5000 | NULL |     10 |
|  8844 | KULDEEP   | SALESMAN  | 8698 | 1991-09-08 00:00:00 | 1500 |    0 |     30 |
|  8886 | ANOOP     | CLERK     | 8888 | 1993-01-12 00:00:00 | 1100 | NULL |     20 |
|  8900 | JATIN     | CLERK     | 8698 | 1991-12-03 00:00:00 |  950 | NULL |     30 |
|  8902 | FAKIR     | ANALYST   | 8566 | 1991-12-03 00:00:00 | 3000 | NULL |     20 |
|  8934 | MITA      | CLERK     | 8882 | 1992-01-02 00:00:00 | 1300 | NULL |     10 |
+-------+-----------+-----------+------+---------------------+------+------+--------+
13 rows in set (0.01 sec)

mysql> 
```
