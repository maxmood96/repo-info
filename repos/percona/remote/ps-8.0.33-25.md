## `percona:ps-8.0.33-25`

```console
$ docker pull percona@sha256:10d613af65784350b2a1c5058eb17a2d2ba10d0bbd659a42105c2672606c6908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0.33-25` - linux; amd64

```console
$ docker pull percona@sha256:36460c4af5e10b81a28b9d04d71c63473ccf6a1cc99ba1d4a0ed4e1bff079f90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851bac0e128c531f59f38ef28ef24f0b7b4a8e1ea515fe3271d425dc305e5df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:04 GMT
ADD file:1b17b1f4725aa932a7091a63de0baa5a5b77b1fc8865bda1797ee0558fd0093b in / 
# Fri, 11 Aug 2023 01:20:05 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:42:00 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:42:01 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_VERSION=8.0.33-25.1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1
# Fri, 11 Aug 2023 01:42:01 GMT
ENV OS_VER=el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_PERCONA_VERSION=8.0.33-25.1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.33-1.el9
# Fri, 11 Aug 2023 01:42:01 GMT
ENV PS_REPO=testing
# Fri, 11 Aug 2023 01:42:04 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Fri, 11 Aug 2023 01:43:01 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Fri, 11 Aug 2023 01:43:05 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Fri, 11 Aug 2023 01:43:05 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Fri, 11 Aug 2023 01:43:05 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 01:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 01:43:05 GMT
USER mysql
# Fri, 11 Aug 2023 01:43:05 GMT
EXPOSE 3306 33060
# Fri, 11 Aug 2023 01:43:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d6f6a69cdebb6617fc05d070c2236a9b1eaa992c5e34728f7351848d9def2981`  
		Last Modified: Fri, 11 Aug 2023 01:21:26 GMT  
		Size: 88.0 MB (87960391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41019feaaa6004a1d7df244a83679dbc15e08d2abf5dc15521a0c038122bfa29`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6903b1768126a5ed2772e84df7add9e284a1662212a9c234c43bfa716c65e3`  
		Last Modified: Fri, 11 Aug 2023 01:49:23 GMT  
		Size: 7.3 MB (7329887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13413b1d6c597ff3bd5c516be02641d5c1bd637296d097b84a7934bcff5512cb`  
		Last Modified: Fri, 11 Aug 2023 01:50:01 GMT  
		Size: 287.8 MB (287754022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f093b4ce6ce3196b59dcb0ec772365acd6937e8147859bd06b0b7e42af1900`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb1b3e47b53ab5e6e7379819c6e2d03f7d656b3e0a7b11691cb027d5dbb8d95`  
		Last Modified: Fri, 11 Aug 2023 01:49:22 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
