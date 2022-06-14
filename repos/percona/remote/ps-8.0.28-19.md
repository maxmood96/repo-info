## `percona:ps-8.0.28-19`

```console
$ docker pull percona@sha256:bf0b2eda005f34a6527b5cbac683d6dd16f34932824ee377228c9f3742d20534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.28-19` - linux; amd64

```console
$ docker pull percona@sha256:fa94c1681062aad9b259c80cf0f94696179ba6607f404cf3b716db314b57ac39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 MB (408016191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048cab045ce6aaf06d6fdcc9b61c0b7e1208f5f41dafff55f9984e0b3c3a7671`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:16 GMT
ADD file:f0e6a328565074e88f761104e323c9f82d10f3a6835f494f792b9550d6c0780c in / 
# Tue, 14 Jun 2022 18:23:17 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:54:39 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 14 Jun 2022 18:54:40 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 14 Jun 2022 18:55:09 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Tue, 14 Jun 2022 18:55:09 GMT
ENV PS_VERSION=8.0.28-19.1
# Tue, 14 Jun 2022 18:55:09 GMT
ENV OS_VER=el8
# Tue, 14 Jun 2022 18:55:10 GMT
ENV FULL_PERCONA_VERSION=8.0.28-19.1.el8
# Tue, 14 Jun 2022 18:55:47 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 14 Jun 2022 18:55:49 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 14 Jun 2022 18:55:49 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 14 Jun 2022 18:55:49 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 18:55:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 18:55:49 GMT
USER mysql
# Tue, 14 Jun 2022 18:55:49 GMT
EXPOSE 3306 33060
# Tue, 14 Jun 2022 18:55:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f658974cd1e22c258b47ec713e6cfe60d8f00ec42264206a49a37bf7193cb96e`  
		Last Modified: Tue, 14 Jun 2022 18:24:03 GMT  
		Size: 84.6 MB (84562622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d7e9a5f74dc36c0de198b657dc76880105c0f6434ceba58babeb3049ad56d9`  
		Last Modified: Tue, 14 Jun 2022 18:59:42 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbc95dea39f4896765342c20433e2314a8d7e0db17e5642fbb3c1cd54df3fdd`  
		Last Modified: Tue, 14 Jun 2022 18:59:51 GMT  
		Size: 148.4 MB (148389585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320a6d9cdb0042a1ee40bf4c60e03cb18e5b84fb85bedc76e629715af1a5d1e4`  
		Last Modified: Tue, 14 Jun 2022 19:00:07 GMT  
		Size: 175.1 MB (175058564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea10fd4ab5b47872b66750ffb1a31a8798cc6b504095446e9ab68957b053fe34`  
		Last Modified: Tue, 14 Jun 2022 18:59:42 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df77008c7208dc08d0ea558e015f9520f17f6c592be26819f45398aca2915e0c`  
		Last Modified: Tue, 14 Jun 2022 18:59:42 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
