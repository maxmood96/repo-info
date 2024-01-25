## `percona:ps-5`

```console
$ docker pull percona@sha256:da4d8be36af72c8e3e9e5307a9b8e4ab4269baf06434c9025254c40c4a738197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:1ad410f4a26e61afef643d0a7c1c97b88fe187677d008cfe0f0feb70be37e74f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453119515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4032ac5474b6db5af9a2139a5933c552d72b1e76f1a1723484394bc8dd89889e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:35 GMT
ADD file:1787cf49c4d22526c303564cb92d6cb59bc8f9682bdff26d62f95661e6319715 in / 
# Wed, 17 Jan 2024 21:34:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 21:54:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 17 Jan 2024 21:54:54 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 17 Jan 2024 21:55:34 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 25 Jan 2024 18:34:07 GMT
ENV PS_VERSION=5.7.44-48.1
# Thu, 25 Jan 2024 18:34:07 GMT
ENV OS_VER=el8
# Thu, 25 Jan 2024 18:34:07 GMT
ENV FULL_PERCONA_VERSION=5.7.44-48.1.el8
# Thu, 25 Jan 2024 18:34:07 GMT
ENV PS_TELEMETRY_VERSION=5.7.44-48-1
# Thu, 25 Jan 2024 18:34:07 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 25 Jan 2024 18:34:07 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 25 Jan 2024 18:34:07 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 25 Jan 2024 18:35:17 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 25 Jan 2024 18:35:19 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 25 Jan 2024 18:35:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 25 Jan 2024 18:35:20 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona
# Thu, 25 Jan 2024 18:35:20 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el8
# Thu, 25 Jan 2024 18:35:20 GMT
COPY file:608e17c8b09b8671bc179eee20453784b46565e804b6fda6e7dd84be5e2eebe3 in /docker-entrypoint.sh 
# Thu, 25 Jan 2024 18:35:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 18:35:20 GMT
USER mysql
# Thu, 25 Jan 2024 18:35:20 GMT
EXPOSE 3306
# Thu, 25 Jan 2024 18:35:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a91077be61e1a167164aba937740c28804e48b3556a604b66999371e107dca2f`  
		Last Modified: Wed, 17 Jan 2024 21:36:37 GMT  
		Size: 100.8 MB (100785243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818c5b060406a3c089e4b076597672fbffddae0ab6e32e7d6e106165127c584`  
		Last Modified: Wed, 17 Jan 2024 22:02:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df382b9ac3bbef7ed95442b9c8c72396d956daf4536a4eb4c473f2d10dcfd94e`  
		Last Modified: Wed, 17 Jan 2024 22:03:07 GMT  
		Size: 214.2 MB (214175417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2f7d859f6d1117c710b437c56eb5e28e1c98dd675f4e3177c45fb5fba4f478`  
		Last Modified: Thu, 25 Jan 2024 18:36:23 GMT  
		Size: 138.1 MB (138148906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16cf56680f4d246009a4a6e2cf8ec240fe1e654861ceb9ee1cc65949d9e682`  
		Last Modified: Thu, 25 Jan 2024 18:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc013db648fbe36761b228f1375f4e150c66500c8825cf4f28bc2791f9baec2`  
		Last Modified: Thu, 25 Jan 2024 18:36:05 GMT  
		Size: 4.1 KB (4064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8185d57ef627f876288884159dc6f578e3b1c40f42af8c3be5c24b737b33a29`  
		Last Modified: Thu, 25 Jan 2024 18:36:05 GMT  
		Size: 3.3 KB (3289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
