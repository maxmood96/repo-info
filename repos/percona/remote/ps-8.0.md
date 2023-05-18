## `percona:ps-8.0`

```console
$ docker pull percona@sha256:e712bc023c387ce0a230ce2d673341280dfe30ded3e4a1363604d520c17250f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:51aac76723feb64580ddcd1060445378c26c499154678ef71b75d5f40a110b06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344597819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da98a06eb68d8c9d923e90cbc5f21e224c88af9ed806fe9cbe0e87039d4f652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 May 2023 17:20:29 GMT
ADD file:a716feb322ba67797d30b521867154dbcd33bd01b92b8334776f33110cd00239 in / 
# Thu, 18 May 2023 17:20:30 GMT
CMD ["/bin/bash"]
# Thu, 18 May 2023 18:00:01 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 18 May 2023 18:00:02 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 18 May 2023 18:00:02 GMT
ENV PS_VERSION=8.0.32-24.1
# Thu, 18 May 2023 18:00:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1
# Thu, 18 May 2023 18:00:02 GMT
ENV OS_VER=el9
# Thu, 18 May 2023 18:00:02 GMT
ENV FULL_PERCONA_VERSION=8.0.32-24.1.el9
# Thu, 18 May 2023 18:00:02 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.32-1.el9
# Thu, 18 May 2023 18:00:02 GMT
ENV PS_REPO=testing
# Thu, 18 May 2023 18:00:05 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 18 May 2023 18:00:49 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 18 May 2023 18:00:52 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 18 May 2023 18:00:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 18 May 2023 18:00:52 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 18 May 2023 18:00:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 May 2023 18:00:52 GMT
USER mysql
# Thu, 18 May 2023 18:00:52 GMT
EXPOSE 3306 33060
# Thu, 18 May 2023 18:00:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3fee8d5933b0f8891f05ad10786810703fa3aa6d141bf99af0f587b6cc44071e`  
		Last Modified: Thu, 18 May 2023 17:21:31 GMT  
		Size: 88.0 MB (87964944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08aa932734508de69290e1e37f2feb32a4342b9083c168b0c5968cfe62e1c5`  
		Last Modified: Thu, 18 May 2023 18:01:28 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d999115ff1c0155ab7f57edf5d02f0e071657d5abc16d0522e669831e2309e5`  
		Last Modified: Thu, 18 May 2023 18:01:29 GMT  
		Size: 7.3 MB (7332929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5fff0b6a72e82305d18a1902ba892fde90257fbba25496398f258267b99dad`  
		Last Modified: Thu, 18 May 2023 18:02:04 GMT  
		Size: 249.3 MB (249294052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fd1bac766180b1c8d46467fdbbaa5467779ac87193786edfc9c8ee8e69e116`  
		Last Modified: Thu, 18 May 2023 18:01:28 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c049dceb0f1e3f5c2b9633fbadd0c9ed3bcc1b643aeef27da0b8c3c0a27eab40`  
		Last Modified: Thu, 18 May 2023 18:01:28 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
