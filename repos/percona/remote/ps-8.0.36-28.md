## `percona:ps-8.0.36-28`

```console
$ docker pull percona@sha256:1128d56e64711ed65cb0c57041048967ee5875a2167d708d327885fd1f995fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.36-28` - linux; amd64

```console
$ docker pull percona@sha256:bdc40b0781c0ef6fb620bc419ee96791ad2bf347df7c24ce365a693b45e1286a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398822232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f11614f8dcfadaf0ee0dad396d997259e1988c262511b959b883ed0a01bb80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jun 2024 19:38:20 GMT
ADD file:87e047bc800fc00e3a773db029c7478e6fda5e2faeeebac9666b8d7a1c289aa2 in / 
# Wed, 26 Jun 2024 19:38:21 GMT
CMD ["/bin/bash"]
# Wed, 26 Jun 2024 19:54:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 26 Jun 2024 19:54:58 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_VERSION=8.0.36-28.1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1
# Wed, 26 Jun 2024 19:54:58 GMT
ENV OS_VER=el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_PERCONA_VERSION=8.0.36-28.1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.36-1.el9
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_REPO=release
# Wed, 26 Jun 2024 19:54:58 GMT
ENV PS_TELEMETRY_VERSION=8.0.36-28-1
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 26 Jun 2024 19:54:59 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 26 Jun 2024 19:54:59 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 26 Jun 2024 19:55:02 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 26 Jun 2024 19:56:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 26 Jun 2024 19:56:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 26 Jun 2024 19:56:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 26 Jun 2024 19:56:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 26 Jun 2024 19:56:21 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 26 Jun 2024 19:56:21 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 26 Jun 2024 19:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 26 Jun 2024 19:56:21 GMT
USER mysql
# Wed, 26 Jun 2024 19:56:21 GMT
EXPOSE 3306 33060
# Wed, 26 Jun 2024 19:56:21 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ccf3affdaddeb9b2b311495d10a59148cb7ceaa3ed52192df2bc3ef3997409aa`  
		Last Modified: Wed, 26 Jun 2024 19:39:31 GMT  
		Size: 95.5 MB (95454973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9444ed0f4c76318d532a3218b097dec3bf5c5fc394c41cf1245249c5362bcb43`  
		Last Modified: Wed, 26 Jun 2024 19:57:09 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9052ffea126e92cb05c563054de4d5ba66de79add3744687f22b27c070cdbd7f`  
		Last Modified: Wed, 26 Jun 2024 19:57:08 GMT  
		Size: 7.3 MB (7323584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538c0b6843d41de068c56cb3f263ac519eb4c810a05903d4f1af00b469bf9f5`  
		Last Modified: Wed, 26 Jun 2024 19:57:48 GMT  
		Size: 296.0 MB (296033629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf3e810c8a8d020e4e1bf103b090554cfb9d1abd4824c3cc6f75ffeb30eb211`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025ba6929159558875c582544f3a15a24c7d50be9aa96378c5679829fd68486`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 4.0 KB (4009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b7c186297e56627b06bc7e92353d7db2c7d257b9d056ebfbea9c7d0f7841c`  
		Last Modified: Wed, 26 Jun 2024 19:57:07 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
