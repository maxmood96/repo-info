## `percona:8-centos`

```console
$ docker pull percona@sha256:fe3be2ef00d68a9ab8fa3dd2128e33186b61b900b31dda4dd9e6f244b122e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:6c14b42f9b58ba747312a54170f82672dd5daeb5ddcf74d7423ba2b10b199f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396596821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b57c125f1de4a3179b021a40a44fc056d8de380ea32ad464c5da98cd1b5589f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 14 Feb 2024 01:46:36 GMT
ADD file:7ea9be7dfb7cfd2abba50070e38c1b9d1de25452ff858e898b76736987280a92 in / 
# Wed, 14 Feb 2024 01:46:37 GMT
CMD ["/bin/bash"]
# Wed, 14 Feb 2024 03:21:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 14 Feb 2024 03:21:35 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 14 Feb 2024 03:21:35 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 14 Feb 2024 03:21:35 GMT
ENV OS_VER=el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 14 Feb 2024 03:21:35 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_REPO=release
# Wed, 14 Feb 2024 03:21:36 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 14 Feb 2024 03:21:36 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 14 Feb 2024 03:21:36 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 14 Feb 2024 03:21:38 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 14 Feb 2024 03:22:50 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 14 Feb 2024 03:22:54 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 14 Feb 2024 03:22:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 14 Feb 2024 03:22:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 14 Feb 2024 03:22:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 14 Feb 2024 03:22:56 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 14 Feb 2024 03:22:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 03:22:56 GMT
USER mysql
# Wed, 14 Feb 2024 03:22:56 GMT
EXPOSE 3306 33060
# Wed, 14 Feb 2024 03:22:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b902d6b6048a1896744bbc0975698dedfbf42b6865b8bd64c26fc06f80e37e36`  
		Last Modified: Wed, 14 Feb 2024 01:48:32 GMT  
		Size: 95.1 MB (95142868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aa560f4034acef426002bd418e8011c1a9288ec9b2d41284274644448e9ed4`  
		Last Modified: Wed, 14 Feb 2024 03:30:08 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5793ec6dae3a828ff94c3950fcacc18b19a1f8323470840bfa844f9cf8ecad93`  
		Last Modified: Wed, 14 Feb 2024 03:30:07 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3a70cce83f9186e13dd1901d435bf8d1ae509dbda3adb0d367ca874d41164`  
		Last Modified: Wed, 14 Feb 2024 03:30:48 GMT  
		Size: 294.2 MB (294153730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b4c4fb71812c0b3208584231132e0078d634473e177b7eb15e9ac2e51cd46`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fb81951f405654947eb3a0dd33087cdcf3edfe3bd33a14a3a71714f81f5e7`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0cb4070be51242262767fe50e048a20613d986046eea27c39486c612fe1a1`  
		Last Modified: Wed, 14 Feb 2024 03:30:06 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
