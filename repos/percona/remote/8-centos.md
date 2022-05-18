## `percona:8-centos`

```console
$ docker pull percona@sha256:9918a56964716260f6812ed1b9d85216cac8a76530ba29c84792feeaf26f3a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:a9b8d22536349ca51c201425293a64c9d2c0286fbaf701db7b6ab106e72bbd3b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.2 MB (406245388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce597e4aa059200d36326468baeb7a67ad7deccd3b42fd4b4948277280d4627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:41:30 GMT
ADD file:eafd9e49bc2d45c1c5bf5571be43743e0500886224b81c0a07dc7c3d1702d7bb in / 
# Tue, 17 May 2022 22:41:30 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:13:01 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 May 2022 23:13:02 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Tue, 17 May 2022 23:13:31 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Tue, 17 May 2022 23:13:31 GMT
ENV PS_VERSION=8.0.28-19.1
# Tue, 17 May 2022 23:13:31 GMT
ENV OS_VER=el8
# Tue, 17 May 2022 23:13:31 GMT
ENV FULL_PERCONA_VERSION=8.0.28-19.1.el8
# Tue, 17 May 2022 23:14:11 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Tue, 17 May 2022 23:14:13 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 17 May 2022 23:14:13 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 17 May 2022 23:14:13 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Tue, 17 May 2022 23:14:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 May 2022 23:14:13 GMT
USER mysql
# Tue, 17 May 2022 23:14:13 GMT
EXPOSE 3306 33060
# Tue, 17 May 2022 23:14:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:25cd53f41add30fe2e87a488316e4bcfbecf123077c0f9f29be5cd359cbafd32`  
		Last Modified: Tue, 17 May 2022 22:42:23 GMT  
		Size: 84.6 MB (84569034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4d816ef18abe5febc4013eb8eb7d738ca8a2442fce3e877883b94559b93263`  
		Last Modified: Tue, 17 May 2022 23:18:11 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f29fe397410972ea5961edb13469d72ded0949c8fe137a3d31301ddd913283b`  
		Last Modified: Tue, 17 May 2022 23:18:20 GMT  
		Size: 146.6 MB (146598899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a07f2f4cba89f96ea781d3182e10ac656bbbda7ab2b1e2b343d21beed3ed2ed`  
		Last Modified: Tue, 17 May 2022 23:18:37 GMT  
		Size: 175.1 MB (175072036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90629578d389926662ac29c1cd5f8a8e93ebdb8f0c1bb5cf369ad6ca4b65f1df`  
		Last Modified: Tue, 17 May 2022 23:18:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d37afb66a84e71493e68d3b13bca6cac568c54dba468844970dab165458bbc1`  
		Last Modified: Tue, 17 May 2022 23:18:11 GMT  
		Size: 3.1 KB (3088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
