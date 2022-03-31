## `percona:ps-8.0`

```console
$ docker pull percona@sha256:291aac4036ef03b6f9cc05a5921052a1d5b3e5412d7e9b253552d7df025f1b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:8491238ee75dddf289ca3b50d8a40f7fb1620b70c0d4cbe15ae24843a61bf0c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.2 MB (387217773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3216da0f7f2b45b31e2b2e4eedb084cbfdc0d0b299e72700978e1ccb9429ce56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:33 GMT
ADD file:d94132182c035117e6c34ac6179798583b0adcdb2790160d2740b5a23dfef57b in / 
# Tue, 29 Mar 2022 18:35:34 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:14:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 31 Mar 2022 02:14:41 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 31 Mar 2022 02:15:08 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Thu, 31 Mar 2022 02:15:09 GMT
ENV PS_VERSION=8.0.27-18.1
# Thu, 31 Mar 2022 02:15:09 GMT
ENV OS_VER=el8
# Thu, 31 Mar 2022 02:15:09 GMT
ENV FULL_PERCONA_VERSION=8.0.27-18.1.el8
# Thu, 31 Mar 2022 02:15:44 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         tzdata         jemalloc         which         cracklib-dicts         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 31 Mar 2022 02:15:46 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 31 Mar 2022 02:15:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 31 Mar 2022 02:15:46 GMT
COPY file:fcc7e1ba857456cd0be5e7e73c551fe742d4b08d93a5cc538710f4731b28e602 in /docker-entrypoint.sh 
# Thu, 31 Mar 2022 02:15:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 31 Mar 2022 02:15:46 GMT
USER mysql
# Thu, 31 Mar 2022 02:15:46 GMT
EXPOSE 3306 33060
# Thu, 31 Mar 2022 02:15:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f194d33a6f3eb80ec1d36f30e468274de9bc57c56876707532a364fe1edb59b7`  
		Last Modified: Tue, 29 Mar 2022 18:36:37 GMT  
		Size: 87.5 MB (87480759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04382ce291551a867fbde30701dfce280d61c9621d57984be5d56ec68aaadea7`  
		Last Modified: Thu, 31 Mar 2022 02:18:21 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adffeea2470a43c0d75e298b1919f0e6a17eeafe6e6bd4632cc870f9807eb435`  
		Last Modified: Thu, 31 Mar 2022 02:18:29 GMT  
		Size: 137.4 MB (137435794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224104ca3bd7068f3d41e45b2c59ba14aaa8c2c50c4fe80e9fccc5a25c4aa96d`  
		Last Modified: Thu, 31 Mar 2022 02:18:45 GMT  
		Size: 162.3 MB (162295793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf20dbcc64bb46eb50dc72b10f19c82aa25dd5dd17235110a3459abb4596514`  
		Last Modified: Thu, 31 Mar 2022 02:18:21 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2eef42611f7967253c5e496ecad474f8a2ad9e3d430b9b0af1aeeddab12fd81`  
		Last Modified: Thu, 31 Mar 2022 02:18:21 GMT  
		Size: 3.1 KB (3089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
