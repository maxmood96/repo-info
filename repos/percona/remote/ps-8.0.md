## `percona:ps-8.0`

```console
$ docker pull percona@sha256:c185f5571b4c5a9a7ad5ba4b157867d493a9eeea67f2e64ea977aa3f8fe7ce07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:cb31468bfdc9240ce59d1f565b35a9eca09de55760ab8046580f8cd43d2e790d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 MB (396606621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec614e99e8928f5bc4cac7b03e760b31609a267e57efa5c48581a71fce8e21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Feb 2024 00:01:58 GMT
ADD file:b70c1c123edf94f63a61ef2e94f83deade5b6d8aa8daeb86f7842df03d15a165 in / 
# Wed, 07 Feb 2024 00:01:59 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 06:41:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 07 Feb 2024 06:41:10 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_VERSION=8.0.35-27.1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.35-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV OS_VER=el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_PERCONA_VERSION=8.0.35-27.1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.35-1.el9
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_REPO=release
# Wed, 07 Feb 2024 06:41:11 GMT
ENV PS_TELEMETRY_VERSION=8.0.35-27-1
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Wed, 07 Feb 2024 06:41:11 GMT
ENV CALL_HOME_VERSION=0.1
# Wed, 07 Feb 2024 06:41:11 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Wed, 07 Feb 2024 06:41:14 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 07 Feb 2024 06:42:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     dnf -y update         curl         glibc         libnghttp2         python3;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 07 Feb 2024 06:42:22 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 07 Feb 2024 06:42:22 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 07 Feb 2024 06:42:23 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Wed, 07 Feb 2024 06:42:23 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Wed, 07 Feb 2024 06:42:23 GMT
COPY file:f14ee89f981aa0851971ffcbb233ebafb523b27fac7a617805e389865ea6dd95 in /docker-entrypoint.sh 
# Wed, 07 Feb 2024 06:42:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Feb 2024 06:42:23 GMT
USER mysql
# Wed, 07 Feb 2024 06:42:23 GMT
EXPOSE 3306 33060
# Wed, 07 Feb 2024 06:42:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7decf94f86e28d15b678b57d429ecedfcbd3ee89bc57b46259f56e87cb427a22`  
		Last Modified: Wed, 07 Feb 2024 00:03:27 GMT  
		Size: 95.1 MB (95146686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac53f4c1a4437c980a08d46df1af43950e251448f096086f0619f87202aada`  
		Last Modified: Wed, 07 Feb 2024 06:49:26 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245cc149398e27063940b17534c4cd50103b19615dee3d74d9a4c6801188d7d`  
		Last Modified: Wed, 07 Feb 2024 06:49:25 GMT  
		Size: 7.3 MB (7289626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f57f6f43025bbd82e0dff6418865322df589144fdd1d4eadaab45af0a18cc3`  
		Last Modified: Wed, 07 Feb 2024 06:50:05 GMT  
		Size: 294.2 MB (294160142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a919541bfce570d0f344f59d16d01d8e6b2859b753683bc81dd99cbc8e651`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8a5fceb8ece6d67ce9b78b9f7e03ce3dac8b2e9c1cd172aca3c3905681486a`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 4.1 KB (4058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f4f355b3d0ab628fcea5589f2d9ad122e1d9271c2b6e47c90d37e8af1d5e3`  
		Last Modified: Wed, 07 Feb 2024 06:49:24 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
