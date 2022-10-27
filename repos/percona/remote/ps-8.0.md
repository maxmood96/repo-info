## `percona:ps-8.0`

```console
$ docker pull percona@sha256:4aeec468e7d7d38c56ac93052ac678fca45a5cb561b923c488d02c50ee4eec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:c914f70b02a2f14f034f8cfb2fccad50fc7da1512a19821c301f9146d41973f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.2 MB (426249216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4a4a4c9857d17100a53646d53a615870b96099db68ab0f0ca1b8d6072b487f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 27 Oct 2022 17:21:34 GMT
ADD file:21d51ed5d75272951d93bd7d363ccf19173ef416b25c6acb627b575293fb7389 in / 
# Thu, 27 Oct 2022 17:21:35 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 17:45:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 27 Oct 2022 17:45:31 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -c "Default Application User" mysql
# Thu, 27 Oct 2022 17:46:01 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     dnf -y module disable mysql;     percona-release disable all;     percona-release enable ps-80 release
# Thu, 27 Oct 2022 17:46:02 GMT
ENV PS_VERSION=8.0.29-21.1
# Thu, 27 Oct 2022 17:46:02 GMT
ENV OS_VER=el8
# Thu, 27 Oct 2022 17:46:02 GMT
ENV FULL_PERCONA_VERSION=8.0.29-21.1.el8
# Thu, 27 Oct 2022 17:46:37 GMT
RUN set -ex;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 27 Oct 2022 17:46:40 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 27 Oct 2022 17:46:40 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 27 Oct 2022 17:46:40 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 27 Oct 2022 17:46:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 Oct 2022 17:46:40 GMT
USER mysql
# Thu, 27 Oct 2022 17:46:40 GMT
EXPOSE 3306 33060
# Thu, 27 Oct 2022 17:46:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1ca7c848b9e5e4ce2ec73f5399f2b0c161b4c592c979bfb25cd1acc15ea0d84a`  
		Last Modified: Thu, 27 Oct 2022 17:23:09 GMT  
		Size: 86.0 MB (85963514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae1552af4f5629bb530211e9901a1ce5ac0edf1130f6bef7756f6734f55990e`  
		Last Modified: Thu, 27 Oct 2022 17:50:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1bcdf57387d9c8c12d4765c840f639dbdb622ee4e7e6f07f23b36510d76093`  
		Last Modified: Thu, 27 Oct 2022 17:50:40 GMT  
		Size: 161.8 MB (161819910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b3bb0bc0356f8051b67844bd2e3bb3e82944e8994c764be3c9787242d899c9`  
		Last Modified: Thu, 27 Oct 2022 17:50:57 GMT  
		Size: 178.5 MB (178460364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e9e8e1c328058e86612503830a19a3098ed1001bc14399bf8ec8807ba28232`  
		Last Modified: Thu, 27 Oct 2022 17:50:31 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e32eb96c5305c4cfd27426dc762a6142533b83bab76b7335868f7ae7b253d6`  
		Last Modified: Thu, 27 Oct 2022 17:50:31 GMT  
		Size: 3.1 KB (3092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
