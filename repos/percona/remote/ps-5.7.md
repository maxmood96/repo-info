## `percona:ps-5.7`

```console
$ docker pull percona@sha256:0f19995a44c099c14a1f11cbed69b3b28711259b45af9b5c117db4d217af2453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:346034384e271a4c441ae53e00924fb21d8ec2519ca4ca7fabd04157c9878f05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 MB (424449091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101d3076abbeb4f9927c1ef5dff3b0daf9715e5e01fded829a5157c356da6524`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Sep 2023 23:23:50 GMT
ADD file:f1400f7c015d009a734ef72b857aca20fa0b646827d6d6c0fbd1ec44314f40f1 in / 
# Thu, 21 Sep 2023 23:23:51 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:45:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 21 Sep 2023 23:45:53 GMT
RUN set -ex;     groupdel ssh_keys;     userdel systemd-coredump;     groupadd -g 999 mysql;     useradd -u 999 -r -g 999 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 21 Sep 2023 23:46:30 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql
# Thu, 21 Sep 2023 23:46:30 GMT
ENV PS_VERSION=5.7.39-42.1
# Thu, 21 Sep 2023 23:46:30 GMT
ENV OS_VER=el8
# Thu, 21 Sep 2023 23:46:30 GMT
ENV FULL_PERCONA_VERSION=5.7.39-42.1.el8
# Thu, 21 Sep 2023 23:47:08 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         Percona-Server-server-57-${FULL_PERCONA_VERSION}         Percona-Server-devel-57-${FULL_PERCONA_VERSION}         Percona-Server-tokudb-57-${FULL_PERCONA_VERSION}         Percona-Server-rocksdb-57-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 21 Sep 2023 23:47:10 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	ln -s /etc/my.cnf.d /etc/mysql; 	chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d; 	chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Thu, 21 Sep 2023 23:47:10 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 21 Sep 2023 23:47:10 GMT
COPY file:905f699d79b77ffbf7039a84326c28f490b5fbb94dacddae8e03ff2d2ee34360 in /docker-entrypoint.sh 
# Thu, 21 Sep 2023 23:47:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Sep 2023 23:47:10 GMT
USER mysql
# Thu, 21 Sep 2023 23:47:10 GMT
EXPOSE 3306
# Thu, 21 Sep 2023 23:47:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f757f4fc3d201c5d7b9b19e3dbf0ddd78af45972be1834845cecc8fe6a2a5c27`  
		Last Modified: Thu, 21 Sep 2023 23:25:04 GMT  
		Size: 89.0 MB (88977617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e3ef28944bbdd6c846a994cd50850e3014c70ac2ad99c711ec463e19d1fcf9`  
		Last Modified: Thu, 21 Sep 2023 23:52:20 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870c60b0c87f562734829269126aa0bb52386d8095ecf72e3380b022ac66aa19`  
		Last Modified: Thu, 21 Sep 2023 23:52:31 GMT  
		Size: 197.9 MB (197926337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa1942d9715497a4d5c8144d9b7e9c0af02aa5123a4caa064575eaa5dd2d378`  
		Last Modified: Thu, 21 Sep 2023 23:52:38 GMT  
		Size: 137.5 MB (137539471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f9825f1b35780a1c129b51997860b996fd55e098b3c08766d7521ee9abf82`  
		Last Modified: Thu, 21 Sep 2023 23:52:20 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5420b26b3a232402873e8da59f18462de8107cba201ec16b1a3b84a0af302c59`  
		Last Modified: Thu, 21 Sep 2023 23:52:20 GMT  
		Size: 3.1 KB (3063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
