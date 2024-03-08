## `percona:ps-5.7.44`

```console
$ docker pull percona@sha256:393966cfe0423c4f05d720c57fad1ea7db7ade52b371ef860f1fa1ee7d6c7707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7.44` - linux; amd64

```console
$ docker pull percona@sha256:f3b9f6286acd66b53235dbb5c5cea613a9a0e0e3fbb06298e1d81299b5492e43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459637383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f363eb0b662469c698574d53dbe410bf65d19c7d5abca7ed4aa7491667715e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:40:05 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Fri, 08 Mar 2024 19:40:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_VERSION=5.7.44-48.1
# Fri, 08 Mar 2024 19:40:44 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Fri, 08 Mar 2024 19:40:44 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 08 Mar 2024 19:40:45 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 08 Mar 2024 19:40:45 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 08 Mar 2024 19:41:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 08 Mar 2024 19:41:24 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Fri, 08 Mar 2024 19:41:24 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 08 Mar 2024 19:41:25 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Fri, 08 Mar 2024 19:41:25 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Fri, 08 Mar 2024 19:41:25 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Fri, 08 Mar 2024 19:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Mar 2024 19:41:25 GMT
USER mysql
# Fri, 08 Mar 2024 19:41:25 GMT
EXPOSE 3306
# Fri, 08 Mar 2024 19:41:26 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5579a2d5bdeb28e11759cd0a76b88d73953c361149b7cafbba31eba2c2937c`  
		Last Modified: Fri, 08 Mar 2024 19:48:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28529cecdfedfe04e8de4a09c403ee2218b0c500da3021b4f8058aeeffe49af0`  
		Last Modified: Fri, 08 Mar 2024 19:48:12 GMT  
		Size: 220.7 MB (220660234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebe5ab283206ab021eba5aa85d375a9869aaa04d8605a86dcf4f3cb8d30df27`  
		Last Modified: Fri, 08 Mar 2024 19:48:18 GMT  
		Size: 138.2 MB (138167207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ed6ba05901e5e5d1ad1305d6e43b56204a2c428ab11cacafb2d06457f18df`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3098f6b4c4804aa2737e552d4414d0d2aaac91896049d748beada45e5e84f58`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753be3494f0cef2bf1f69afd17e8f94d4a0ece70aa5b578029996a01d55651`  
		Last Modified: Fri, 08 Mar 2024 19:48:00 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
