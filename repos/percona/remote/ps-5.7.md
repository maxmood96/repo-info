## `percona:ps-5.7`

```console
$ docker pull percona@sha256:6cf486b5bc6055f1bb56953984e04558c4fc589dde67054c12439e1bed0201b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:64c77f30070bcc1f62929f8fcfb47c0ca9581792cf33d3ab578789a70290ee03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454073870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e56490dd078a74f6c8217ccee28ff387724c238df3918e8537c9b88b75edb54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:02:24 GMT
ADD file:7ca18ea735b6b1e0c791537b71e557d98c4423b3ae347e122256c132a06cfc9b in / 
# Wed, 07 Feb 2024 00:02:24 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:42:34 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:42:34 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:43:13 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 07 Feb 2024 06:43:13 GMT
ENV PS_VERSION=5.7.44-48.1
# Wed, 07 Feb 2024 06:43:13 GMT
ENV OS_VER=el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Wed, 07 Feb 2024 06:43:14 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:43:14 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:43:14 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:43:53 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:43:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 07 Feb 2024 06:43:55 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:43:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:43:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Wed, 07 Feb 2024 06:43:56 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:43:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:43:56 GMT
USER mysql
# Wed, 07 Feb 2024 06:43:56 GMT
EXPOSE 3306
# Wed, 07 Feb 2024 06:43:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:47c5569e59ac36fb6d021ea238638d7fc2b5be604b144913aab75e00e3c2c6e9`  
		Last Modified: Wed, 07 Feb 2024 00:03:58 GMT  
		Size: 100.8 MB (100783216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7441126825829d2291df903cd3b95235b40cd2032f6f4c5d6a4598e751523c`  
		Last Modified: Wed, 07 Feb 2024 06:50:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb58d754bda660fbcc709d09f48ff12b0ab3646527c91e2a471acfe1d38243a`  
		Last Modified: Wed, 07 Feb 2024 06:50:39 GMT  
		Size: 215.1 MB (215134387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb58703da187da72249afafaa01cb41eb5b4a656e4e4404a34da1204087198`  
		Last Modified: Wed, 07 Feb 2024 06:50:46 GMT  
		Size: 138.1 MB (138146317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5013e5831d104812263b37cb7ceaf06039bd5d511955827ac3ecbd4a666224`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c3213114431a4ed35c3e1caa9724afe4a94375934a807c45d5407c2d64dad`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 4.1 KB (4057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed00d604ae350ff4966f9d7e0904eabf741cb0a6a40c66c0e0b40909efb0f1b`  
		Last Modified: Wed, 07 Feb 2024 06:50:27 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
