## `percona:ps-8`

```console
$ docker pull percona@sha256:485704cb39d9e72ce525d67ab59fb83453de15f9312098a910cd7385179dab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:b81858bde8fbf62f1e90a82bfa12a663d1d831328d7919a0301ba1319742523d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394633135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5a5a084433c2bc56bcf4ce50e38789dfa853261f8c93d4299eb605f073d70f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:05 GMT
ADD file:920518e549f43e1b0c849a61c59579bb90aa4a66c593f0af57541bcd6500ff02 in / 
# Wed, 17 Jan 2024 21:34:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:53:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:53:31 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:53:31 GMT
ENV PS_VERSION=8.0.34-26.1
# Wed, 17 Jan 2024 21:53:31 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Wed, 17 Jan 2024 21:53:31 GMT
ENV OS_VER=el9
# Wed, 17 Jan 2024 21:53:31 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Wed, 17 Jan 2024 21:53:31 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Wed, 17 Jan 2024 21:53:31 GMT
ENV PS_REPO=release
# Wed, 17 Jan 2024 21:53:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 17 Jan 2024 21:54:37 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 17 Jan 2024 21:54:42 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 17 Jan 2024 21:54:42 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 17 Jan 2024 21:54:42 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Wed, 17 Jan 2024 21:54:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 21:54:42 GMT
USER mysql
# Wed, 17 Jan 2024 21:54:42 GMT
EXPOSE 3306 33060
# Wed, 17 Jan 2024 21:54:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5a38b24651b5364733d618ef523ef69447763bf41bf2a2198da479782daa5f44`  
		Last Modified: Wed, 17 Jan 2024 21:36:04 GMT  
		Size: 95.1 MB (95137236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfb3be153ed9a7566a289b1f1d7f6aa214ce663a31c74cc4fc5a42bcb8807e1`  
		Last Modified: Wed, 17 Jan 2024 22:01:50 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cbd92a793681878b7814c067ecce755fda1dffbc83fdb068def97e5b6a1e5d`  
		Last Modified: Wed, 17 Jan 2024 22:01:51 GMT  
		Size: 7.3 MB (7292594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0de14c1f24e5c3a33c38fb8da696b1427fa7c6180485e6c69c7d14c711f3570`  
		Last Modified: Wed, 17 Jan 2024 22:02:31 GMT  
		Size: 292.2 MB (292197429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633c2233b1bf7ea0c702106cd0eb66aa65f016fb50816cbc29e6c88b1638ceef`  
		Last Modified: Wed, 17 Jan 2024 22:01:50 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb6d650d245e83ac097822e4951f15c4e63fc47ac26ff8b9a52e874e21c9068`  
		Last Modified: Wed, 17 Jan 2024 22:01:50 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
