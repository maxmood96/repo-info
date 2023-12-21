## `percona:centos`

```console
$ docker pull percona@sha256:aa38883224dd097b3f27959f76a850d623a12333742426354ce0fb97e68b6ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:250e1201e89b29f7763d0b6aee27f65110baa865c7f71c983ace7647d6a80675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 MB (450837133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011b4ddc6a89e5bb8dfcc6fdd9c322644635b167aff67ed5fc8d6e3abcae29c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:40 GMT
ADD file:87f2e99b547675dcdc67b0cfb2faffb906556448d475c79e5862f637c289ca33 in / 
# Wed, 20 Dec 2023 22:40:40 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 23:17:38 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 20 Dec 2023 23:17:39 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Wed, 20 Dec 2023 23:18:20 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Wed, 20 Dec 2023 23:18:20 GMT
ENV PS_VERSION=5.7.43-47.1
# Wed, 20 Dec 2023 23:18:20 GMT
ENV OS_VER=el8
# Wed, 20 Dec 2023 23:18:21 GMT
ENV FULL_PERCONA_VERSION=5.7.43-47.1.el8
# Wed, 20 Dec 2023 23:19:03 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 20 Dec 2023 23:19:04 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Wed, 20 Dec 2023 23:19:04 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 20 Dec 2023 23:19:04 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Wed, 20 Dec 2023 23:19:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Dec 2023 23:19:05 GMT
USER mysql
# Wed, 20 Dec 2023 23:19:05 GMT
EXPOSE 3306
# Wed, 20 Dec 2023 23:19:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:34b9796be6f7b4416c84bc05dd856b62641b1670a2137f15bcefd76b682a2d57`  
		Last Modified: Wed, 20 Dec 2023 22:41:46 GMT  
		Size: 100.8 MB (100784616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d4cd4b3c6679e0ba66d0ec6b08a356753aaba20604b935cf7935804defd6ee`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f63f5912a1dbc77b2f3358a8d97e81eed586231a7de0fddc1a740e5111d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:46 GMT  
		Size: 211.9 MB (211894364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a72cfb8383cb3b47283eb5c7bfad4acaa87b7e4a6b3cbfd91539fa568a9158`  
		Last Modified: Wed, 20 Dec 2023 23:24:53 GMT  
		Size: 138.2 MB (138152481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527f28b140f98118c158a6ceae22df6201ed35a80d7bf661e558bb1d71caf5b`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21e17b32a67e3122bd49f3605d6c20b000f413ab89e72a19113cf134045b38`  
		Last Modified: Wed, 20 Dec 2023 23:24:34 GMT  
		Size: 3.1 KB (3064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
