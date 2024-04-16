## `percona:ps-5`

```console
$ docker pull percona@sha256:4924cf26d330d308b09c93b0d90bc78f6ac335e7b7577452c8f1ca57e9a7a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:3f04d74a14426b9cd7c15d6d0be2cf9a0e0173ba3ff2852feb1e69c53b1ec36b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463805642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d951464f6ab9c90dc745d562c7e3f815d2344c90a9a9d111767d0773c95bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:19 GMT
ADD file:2e1f3bac70f203a89b11ea95678959e981caebd3f1f6ba35c3d4206a8e313381 in / 
# Tue, 16 Apr 2024 19:54:20 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 20:11:23 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 16 Apr 2024 20:11:24 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 16 Apr 2024 20:12:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Tue, 16 Apr 2024 20:12:05 GMT
ENV PS_VERSION=5.7.44-48.1
# Tue, 16 Apr 2024 20:12:05 GMT
ENV OS_VER=el8
# Tue, 16 Apr 2024 20:12:05 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Tue, 16 Apr 2024 20:12:06 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 16 Apr 2024 20:12:06 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 16 Apr 2024 20:12:06 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 16 Apr 2024 20:12:46 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 16 Apr 2024 20:12:48 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 16 Apr 2024 20:12:48 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 16 Apr 2024 20:12:49 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Tue, 16 Apr 2024 20:12:49 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Tue, 16 Apr 2024 20:12:49 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Tue, 16 Apr 2024 20:12:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 20:12:49 GMT
USER mysql
# Tue, 16 Apr 2024 20:12:49 GMT
EXPOSE 3306
# Tue, 16 Apr 2024 20:12:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c2be9dbf3fbcc2fd00c1a899133096fbac0992fc75622b99eb6fb89678b5c50`  
		Last Modified: Tue, 16 Apr 2024 19:55:29 GMT  
		Size: 100.8 MB (100801699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae581c6d33122a75f918ba99c344363cb204eba990a346551847f810fb924f4f`  
		Last Modified: Tue, 16 Apr 2024 20:18:26 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b928f2f02c2d6b14c40d4d6e319660c36b7ae9615426e44813dc94d83f3c0`  
		Last Modified: Tue, 16 Apr 2024 20:18:36 GMT  
		Size: 224.8 MB (224838212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f395eff2ca53dc589e763a108ea80bc0ddde8f6581a23ac65ac4aa911e1a5d9`  
		Last Modified: Tue, 16 Apr 2024 20:18:42 GMT  
		Size: 138.2 MB (138155780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc6d056dcddc89891559e27df05320332428f0201f3c55e19a8ed1f3ecb6bdf`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d64a6a4bc33b24dcf40ac8a64f1626b83a3ee77710a0a766f927156f5a564`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 4.1 KB (4060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff633690d0f942004faa5a914f1c30f34e24f7470babd146ff8e9ebaf85e169e`  
		Last Modified: Tue, 16 Apr 2024 20:18:23 GMT  
		Size: 3.3 KB (3286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
