## `percona:ps-8.0`

```console
$ docker pull percona@sha256:eea067bf09073b6244ad8f2edf1c2e52313a69157af3aae0a2fdd0dcda47af9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:2ee55e6af3c31c86eab57ceb3124bf46a7ecab4432dfb9059c10f12a30825d35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402728336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffc2f9668de60ed3bc8144196024b06dbd9ba7a5f7665cb32e5f9836c5caab6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 May 2022 20:50:56 GMT
ADD file:84bf324680059e085907eb7d75c8cb37d4d01aff3cc8241463bbc7d042db93d9 in / 
# Mon, 02 May 2022 20:50:56 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 21:18:32 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 02 May 2022 21:18:33 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Mon, 02 May 2022 21:19:01 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Fri, 13 May 2022 18:19:56 GMT
ENV PS_VERSION=8.0.28-19.1
# Fri, 13 May 2022 18:19:57 GMT
ENV OS_VER=el8
# Fri, 13 May 2022 18:19:57 GMT
ENV FULL_PERCONA_VERSION=8.0.28-19.1.el8
# Fri, 13 May 2022 18:20:54 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 13 May 2022 18:20:56 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 13 May 2022 18:20:56 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 13 May 2022 18:20:56 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 13 May 2022 18:20:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 13 May 2022 18:20:56 GMT
USER mysql
# Fri, 13 May 2022 18:20:56 GMT
EXPOSE 3306 33060
# Fri, 13 May 2022 18:20:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:42405d186b2e7939aa51dc1bcc0f4cf0ce1236f4d6e38f2fae9822c41e98078e`  
		Last Modified: Mon, 02 May 2022 20:51:41 GMT  
		Size: 87.5 MB (87479695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117445dd717bfd25b84ff3228f7acd9d03798f3657b9079a8c68ef3c560b5291`  
		Last Modified: Mon, 02 May 2022 21:23:21 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7b40c38741c4d70f8e0f21960f22f1e7d61b72b918a554cef8e76a21de110d`  
		Last Modified: Mon, 02 May 2022 21:23:29 GMT  
		Size: 140.1 MB (140092189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99454f75348dd9261690f11d24bccb2e8f02f20500a7e9e5f75da1759517707`  
		Last Modified: Fri, 13 May 2022 18:22:19 GMT  
		Size: 175.2 MB (175151034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef841d02d2cd946cdfacde3a78843b4fe2f5117799786ea987971e2693220ed1`  
		Last Modified: Fri, 13 May 2022 18:21:53 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f63090afd8e359bd2fbceaec3567fe8f4c1b77bd2e6b835432fe3f86ee96e4f`  
		Last Modified: Fri, 13 May 2022 18:21:54 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
