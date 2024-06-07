## `percona:centos`

```console
$ docker pull percona@sha256:c93cff42702f0f94477c1ddc8ee36784e8bfd8c91bbe6be9126f1fb2461fcd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:32f501d97a88c1bd1ef5dcc7a2ef889960c04f4aeb1567a390c302223363be39
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474616866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31119c3004f0632d2d674d9e9f585bb1b88d401956b401666f38c4e580312b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:42 GMT
ADD file:0a3a9e560f49471ac4b4a04d79e5a1656dcd3d69171fba02bbe289545bb48815 in / 
# Fri, 07 Jun 2024 03:48:42 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:58:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 07 Jun 2024 04:58:01 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 07 Jun 2024 04:58:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV OS_VER=el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 07 Jun 2024 04:58:45 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 07 Jun 2024 04:58:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 07 Jun 2024 04:58:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 07 Jun 2024 04:59:27 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 07 Jun 2024 04:59:29 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 07 Jun 2024 04:59:29 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 07 Jun 2024 04:59:30 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 07 Jun 2024 04:59:30 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 07 Jun 2024 04:59:30 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 07 Jun 2024 04:59:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 07 Jun 2024 04:59:30 GMT
USER mysql
# Fri, 07 Jun 2024 04:59:31 GMT
EXPOSE 3306
# Fri, 07 Jun 2024 04:59:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:adaa90b6e671c8dbb4f88a663eaaed9a3ddd87cbc357d4e20b81dbd79ad86375`  
		Last Modified: Fri, 07 Jun 2024 03:49:48 GMT  
		Size: 100.7 MB (100715124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2396af4d3b205f9969bae20eae0d37a26816620af86838f9d0fe5b6635409`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369b4b94dd4d955befbe0941c561b11e93b0115a5185fed2176932a562ae035`  
		Last Modified: Fri, 07 Jun 2024 05:05:22 GMT  
		Size: 235.7 MB (235677708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a578b1dc8dace3f7ecb2b2ad6ae5228d1b4b4c1f653e762496c8356e6556404c`  
		Last Modified: Fri, 07 Jun 2024 05:05:28 GMT  
		Size: 138.2 MB (138214191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0650cd95e06f5a256134e78a3b6f351830a99680d9009a55b47c1950ce394aee`  
		Last Modified: Fri, 07 Jun 2024 05:05:12 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44200354a911664ef3510beda8d4faead156ad452f2ace067f9ffd94ee14e468`  
		Last Modified: Fri, 07 Jun 2024 05:05:11 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c56ea828e3885299bc7087c55a355c99b59f934acd70217fbc6c41cea4e2ab`  
		Last Modified: Fri, 07 Jun 2024 05:05:10 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
