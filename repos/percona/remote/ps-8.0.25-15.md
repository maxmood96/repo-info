## `percona:ps-8.0.25-15`

```console
$ docker pull percona@sha256:01a62b5754ea0060bf49ddc3412e81c694ab18311febc1a6b6080dd334c72173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-8.0.25-15` - linux; amd64

```console
$ docker pull percona@sha256:5bc1c13c8f4adfd76ceaac425877e2de2fcd9c33ab685c639e55b23e97eb0c0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260132366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfca7980150a0952b3e6b948444da6e7f0b1ff39343b896b75be03a4d7ab40d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 08 Dec 2020 00:22:52 GMT
ADD file:bd7a2aed6ede423b719ceb2f723e4ecdfa662b28639c8429731c878e86fb138b in / 
# Tue, 08 Dec 2020 00:22:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201204
# Tue, 08 Dec 2020 00:22:53 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 01:08:18 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 06 Mar 2021 01:08:19 GMT
RUN groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 13 Jul 2021 18:36:43 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release setup -y ps80
# Tue, 13 Jul 2021 18:36:44 GMT
ENV PS_VERSION=8.0.25-15.1
# Tue, 13 Jul 2021 18:36:44 GMT
ENV OS_VER=el8
# Tue, 13 Jul 2021 18:36:44 GMT
ENV FULL_PERCONA_VERSION=8.0.25-15.1.el8
# Tue, 13 Jul 2021 18:37:17 GMT
RUN set -ex;     dnf install -y         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-tokudb-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         jemalloc         which         cracklib-dicts         policycoreutils;         dnf clean all;     rm -rf /var/cache/dnf /var/lib/mysql
# Tue, 13 Jul 2021 18:37:19 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 13 Jul 2021 18:37:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 13 Jul 2021 18:37:19 GMT
COPY file:fcc7e1ba857456cd0be5e7e73c551fe742d4b08d93a5cc538710f4731b28e602 in /docker-entrypoint.sh 
# Tue, 13 Jul 2021 18:37:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jul 2021 18:37:20 GMT
USER mysql
# Tue, 13 Jul 2021 18:37:20 GMT
EXPOSE 3306 33060
# Tue, 13 Jul 2021 18:37:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7a0437f04f83f084b7ed68ad9c4a4947e12fc4e1b006b38129bac89114ec3621`  
		Last Modified: Tue, 08 Dec 2020 00:23:32 GMT  
		Size: 75.2 MB (75181999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a7a012c29accf794835ce11206a3b56db3e32217ddef0162311905e5d5da2`  
		Last Modified: Sat, 06 Mar 2021 01:14:30 GMT  
		Size: 1.6 KB (1572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d001e89e27c9b912af12beca0d999f6436c4e952b489b5d039da8014238095d`  
		Last Modified: Tue, 13 Jul 2021 18:38:16 GMT  
		Size: 23.6 MB (23609510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6183e775dcd3b38183ffed92212a38e656b5d2b8df9a22332bb5104caf39936f`  
		Last Modified: Tue, 13 Jul 2021 18:38:40 GMT  
		Size: 161.3 MB (161335031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8fd78d7df974e6a78eb74abf6df632e7a39146b4ba787122cf0097b4fee7ef`  
		Last Modified: Tue, 13 Jul 2021 18:38:14 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf89ad2e329b047f2c0040f3a8808f707c36fa22338e52b4236766af37b62ecb`  
		Last Modified: Tue, 13 Jul 2021 18:38:14 GMT  
		Size: 3.1 KB (3089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
