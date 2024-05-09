## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:2a4dec82b0e9f86fd27254f1d06eb239c050a61fded14d520ec3fcf9bc01f7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:8bfe243a61f4f374b90bc8d5b07c3d18ec000ee17a3eff21994dbbd7c5d49f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464883540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4575458eed1f7fc3e8db3a47ed8835adb862c6b5723d5a3e845760327125a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 09 May 2024 22:30:35 GMT
ADD file:46797d9a8df88ff50077a34274dacf63148250ebdbdc1f1f24df5a9f98785730 in / 
# Thu, 09 May 2024 22:30:36 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 22:49:46 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 09 May 2024 22:49:47 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 09 May 2024 22:50:27 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 09 May 2024 22:50:28 GMT
ENV OS_VER=el8
# Thu, 09 May 2024 22:50:28 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 09 May 2024 22:50:28 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 09 May 2024 22:50:28 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 09 May 2024 22:50:28 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 09 May 2024 22:51:07 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 09 May 2024 22:51:09 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 09 May 2024 22:51:09 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 09 May 2024 22:51:10 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 09 May 2024 22:51:10 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 09 May 2024 22:51:10 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 09 May 2024 22:51:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2024 22:51:10 GMT
USER mysql
# Thu, 09 May 2024 22:51:10 GMT
EXPOSE 3306
# Thu, 09 May 2024 22:51:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03f26a7e823673b1c8552416a19a3b2a8626fd3d07fdb72fe561d4750ec5150f`  
		Last Modified: Thu, 09 May 2024 22:32:22 GMT  
		Size: 100.8 MB (100801054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512982940e3a9962abe8ee679248d16c92f7ed74aa590d53c4bdc05543a4694`  
		Last Modified: Thu, 09 May 2024 22:57:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1df716cd25e496fe1baed61148bab483c6fc187df912d1741176374e5538e3`  
		Last Modified: Thu, 09 May 2024 22:57:59 GMT  
		Size: 225.9 MB (225921560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89875023ed9566f063f265c065c782cb7970b1b05ff97025021f3f45fe1cd584`  
		Last Modified: Thu, 09 May 2024 22:58:05 GMT  
		Size: 138.2 MB (138150971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9733f31218c61a49af239e54dd0dd9730da668f116f51ede3b742ff45a3f55ad`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f5ecd393e93c1f18a417cfd009f3bafd7ae47a02a718f47b759e596ae1f7ff`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 4.1 KB (4061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd669a9f22ee6f75fe56192cf8df67d6d2f9407db91b4bf5934be0397b8cf2d3`  
		Last Modified: Thu, 09 May 2024 22:57:47 GMT  
		Size: 3.3 KB (3288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
