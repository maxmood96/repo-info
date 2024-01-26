## `percona:ps-8.0`

```console
$ docker pull percona@sha256:ce94f718d8ae40179243c1cb79127c7545841457b0b3a30f0a04ae84773b17f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:a0bdaa3326598ca0c8d0c8a34761e48e93fe4699cd93b588bf6a19844409c3d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 MB (394626690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bf6193ccbe84c65161dcc684923e136a1c51a6448bb3db59695ad55a656522`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Jan 2024 01:27:05 GMT
ADD file:c81f9b458346a6ec7c2af51d9fd80df0afd0043030c5e5df5b3a2d01b79f4a60 in / 
# Fri, 26 Jan 2024 01:27:06 GMT
CMD ["/bin/bash"]
# Fri, 26 Jan 2024 02:18:44 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 26 Jan 2024 02:18:45 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 26 Jan 2024 02:18:45 GMT
ENV PS_VERSION=8.0.34-26.1
# Fri, 26 Jan 2024 02:18:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Fri, 26 Jan 2024 02:18:45 GMT
ENV OS_VER=el9
# Fri, 26 Jan 2024 02:18:45 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Fri, 26 Jan 2024 02:18:45 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Fri, 26 Jan 2024 02:18:45 GMT
ENV PS_REPO=release
# Fri, 26 Jan 2024 02:18:47 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 26 Jan 2024 02:19:53 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 26 Jan 2024 02:19:57 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 26 Jan 2024 02:19:57 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 26 Jan 2024 02:19:58 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 26 Jan 2024 02:19:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Jan 2024 02:19:58 GMT
USER mysql
# Fri, 26 Jan 2024 02:19:58 GMT
EXPOSE 3306 33060
# Fri, 26 Jan 2024 02:19:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8f7429f2f24a5384e353c9b32bdb95ad16e06422c83beedbfaf1d4f4ae48d0e6`  
		Last Modified: Fri, 26 Jan 2024 01:28:21 GMT  
		Size: 95.1 MB (95136730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e43a6984bddf0bcfa04e0a0ead898556d3479706315fa16e7cd75af1852af0e`  
		Last Modified: Fri, 26 Jan 2024 02:20:38 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03894787f7552a3b1b99949eec48f5abb6033642d3ad4dbb8a52b1d4e032435e`  
		Last Modified: Fri, 26 Jan 2024 02:20:39 GMT  
		Size: 7.3 MB (7289810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b9c0dea83a2166154268f1a9267e381639f7fbceb562f09a11d158041e5f9c`  
		Last Modified: Fri, 26 Jan 2024 02:21:20 GMT  
		Size: 292.2 MB (292194268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef49593a1a5ca4ac5c4f43723451f48a2ca9c6b10208c0c731272ffb568f3e19`  
		Last Modified: Fri, 26 Jan 2024 02:20:38 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c01f60f41b9965c814d3e4ea74dfc956ad99f4e5a42b6af82599233afe5bb48`  
		Last Modified: Fri, 26 Jan 2024 02:20:38 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
