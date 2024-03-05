## `percona:8-centos`

```console
$ docker pull percona@sha256:88a1088b1d166fb2d69629827031ee0b5a1aa0e1792cd0dc16d8363434892a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:55dfb07d55897d8a3aab5dfb7f5d015c592df087848c7b18f1f2daaa99910e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403414639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884843a80cb097ebe0d86634564f3a754ed26f54e5066e85d99728c4ed0e24d5`
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
# Tue, 05 Mar 2024 01:28:45 GMT
ENV PS_VERSION=8.0.36-28.1
# Tue, 05 Mar 2024 01:28:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Tue, 05 Mar 2024 01:28:45 GMT
ENV OS_VER=el9
# Tue, 05 Mar 2024 01:28:45 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Tue, 05 Mar 2024 01:28:45 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Tue, 05 Mar 2024 01:28:45 GMT
ENV PS_REPO=release
# Tue, 05 Mar 2024 01:28:45 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Tue, 05 Mar 2024 01:28:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 05 Mar 2024 01:28:45 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 05 Mar 2024 01:28:46 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 05 Mar 2024 01:28:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Tue, 05 Mar 2024 01:29:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 05 Mar 2024 01:29:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 05 Mar 2024 01:29:56 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 05 Mar 2024 01:29:57 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 05 Mar 2024 01:29:57 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 05 Mar 2024 01:29:57 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Tue, 05 Mar 2024 01:29:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Mar 2024 01:29:57 GMT
USER mysql
# Tue, 05 Mar 2024 01:29:57 GMT
EXPOSE 3306 33060
# Tue, 05 Mar 2024 01:29:57 GMT
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
	-	`sha256:9c5f58bf93db6e1d2580dfb96747f8ef099ff4763777a40e3302d146bcc1d9c2`  
		Last Modified: Tue, 05 Mar 2024 01:30:53 GMT  
		Size: 7.3 MB (7290057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a551d38a25789e60bbfb23e6a4bdf8ec5d0356f4fe942bc19e8e64c3a729b4d6`  
		Last Modified: Tue, 05 Mar 2024 01:31:35 GMT  
		Size: 301.0 MB (300971543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0864a20667cc31a9d16b43298bbb9724d7c68c0a74709888e7764befbf098c6b`  
		Last Modified: Tue, 05 Mar 2024 01:30:52 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efc5c9218dddae7a56f0893b61ae5b7de7e7a2ae4eea76054027edd758aec0d`  
		Last Modified: Tue, 05 Mar 2024 01:30:52 GMT  
		Size: 4.1 KB (4059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44f3c2bcab54d6fa03d23e102a7bf8ecee656e34ae60bcff63ee5158bd85e31`  
		Last Modified: Tue, 05 Mar 2024 01:30:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
