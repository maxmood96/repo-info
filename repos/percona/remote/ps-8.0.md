## `percona:ps-8.0`

```console
$ docker pull percona@sha256:cef90022611e20b77a517b1778981402b9dc2de33853e3c485bb45c5054c9b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:3f8e55b1d873dfb5c106f52575dabd21334e5cdc93ebf242a8d96b926f2e9dbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398515550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1ea7af2b65c8fc3207c217589d2fc830a00d6e7a9a90288a3933e37894ef19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:12 GMT
ADD file:f364e0004eec4f66e8461b80aca1a10bfbab0511e35e780e31609fcf93057c9c in / 
# Thu, 25 Apr 2024 01:42:13 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 02:09:53 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 25 Apr 2024 02:09:53 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 25 Apr 2024 02:09:53 GMT
ENV PS_VERSION=8.0.36-28.1
# Thu, 25 Apr 2024 02:09:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Thu, 25 Apr 2024 02:09:53 GMT
ENV OS_VER=el9
# Thu, 25 Apr 2024 02:09:54 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Thu, 25 Apr 2024 02:09:54 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Thu, 25 Apr 2024 02:09:54 GMT
ENV PS_REPO=release
# Thu, 25 Apr 2024 02:09:54 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Thu, 25 Apr 2024 02:09:54 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 25 Apr 2024 02:09:54 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 25 Apr 2024 02:09:54 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 25 Apr 2024 02:09:57 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 25 Apr 2024 02:11:11 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Apr 2024 02:11:16 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 25 Apr 2024 02:11:16 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Apr 2024 02:11:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 25 Apr 2024 02:11:18 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 25 Apr 2024 02:11:18 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 02:11:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 02:11:18 GMT
USER mysql
# Thu, 25 Apr 2024 02:11:18 GMT
EXPOSE 3306 33060
# Thu, 25 Apr 2024 02:11:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3dd1469a0b0bcdf2d48ebe5b7be0f55c6f82fe3a3f04374b8953497f46d0ce64`  
		Last Modified: Thu, 25 Apr 2024 01:43:43 GMT  
		Size: 95.2 MB (95164906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41929da165378ddb24461ce49b1c51f11cca9a20c0470aa2f6551509846da6ed`  
		Last Modified: Thu, 25 Apr 2024 02:12:04 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcb5ad9b6cd4246f108090d8471d680417a73fd1d1162428471107553708b59`  
		Last Modified: Thu, 25 Apr 2024 02:12:04 GMT  
		Size: 7.3 MB (7312333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef48cc36abc15a3e6e16073b7f95d9a4a42657f6e4725fb0a93a4b373db992a`  
		Last Modified: Thu, 25 Apr 2024 02:12:45 GMT  
		Size: 296.0 MB (296028144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856e4e5cb821ba2331138cbb11d61dd2bc5f0bfa3853c30b0fe51076d66dad51`  
		Last Modified: Thu, 25 Apr 2024 02:12:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd69efdd0baa5f6471052ec73f0892e4b0e66908c1e71cce40e2e9a6f61d6e6`  
		Last Modified: Thu, 25 Apr 2024 02:12:03 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6e520560ca9bfd94c06b8c95a8f855b29ec8aa27f3379d6ea59b20b9dcf083`  
		Last Modified: Thu, 25 Apr 2024 02:12:03 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
