## `percona:8-centos`

```console
$ docker pull percona@sha256:2956c07b3aa788c3382b9a89aa22d5528c351f6106ffc0faa8839eeb943b754c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:0e067f008e673b31b7c44ecad2586dc4cdcca3e182495b0fead0f585eccb3d9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345346056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046d1d26abeecfb9c29029ca7b4daf74e5a79d75a8894469f5e6c8d2c38bfcd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 22:28:09 GMT
ADD file:45ed45a0e96a01a7bd5f867e49b563e7fb37d1853ea05528cdb7d58aae320652 in / 
# Fri, 31 Mar 2023 22:28:10 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:14:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 31 Mar 2023 23:14:55 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 31 Mar 2023 23:14:55 GMT
ENV PS_VERSION=8.0.32-24.1
# Fri, 31 Mar 2023 23:14:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1
# Fri, 31 Mar 2023 23:14:55 GMT
ENV OS_VER=el9
# Fri, 31 Mar 2023 23:14:55 GMT
ENV FULL_PERCONA_VERSION=8.0.32-24.1.el9
# Fri, 31 Mar 2023 23:14:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.32-1.el9
# Fri, 31 Mar 2023 23:14:56 GMT
ENV PS_REPO=testing
# Fri, 31 Mar 2023 23:14:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 31 Mar 2023 23:15:38 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 31 Mar 2023 23:15:41 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 31 Mar 2023 23:15:41 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 31 Mar 2023 23:15:41 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 31 Mar 2023 23:15:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Mar 2023 23:15:41 GMT
USER mysql
# Fri, 31 Mar 2023 23:15:41 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 23:15:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b23d267b340cf3b374e014207d7edb40b5d712b1c6074d297a7485c531b99608`  
		Last Modified: Fri, 31 Mar 2023 22:29:23 GMT  
		Size: 88.6 MB (88599065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d43be17865422c901be5b096bd1df99d748d920194393c63a9580b2340f28dd`  
		Last Modified: Fri, 31 Mar 2023 23:18:59 GMT  
		Size: 1.6 KB (1632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec78bd254cf2dd2fd15741e9a7b8a9c64190c7cb23eaff2b2daf9ef04bb2f39`  
		Last Modified: Fri, 31 Mar 2023 23:19:00 GMT  
		Size: 7.4 MB (7373737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5d51a333820097acd78a6a0b394f456025a3a5cf55d44441fb8291207ec7e2`  
		Last Modified: Fri, 31 Mar 2023 23:19:31 GMT  
		Size: 249.4 MB (249367368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccde4f29b91a3b3a21212258b76160194b750f7bb04716faf070ef8a744fb22`  
		Last Modified: Fri, 31 Mar 2023 23:18:59 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048b658cd68640cd7515db4cb9cbab7f7bd1fb524e797f2e45da6910799e7de9`  
		Last Modified: Fri, 31 Mar 2023 23:18:59 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
