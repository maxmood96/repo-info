## `percona:ps-8.0`

```console
$ docker pull percona@sha256:f7f4e0ef666b51778edfc0ffe9dd05a69394430d05cd204d895056107b2610fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:5332a2dd238486f597566403403410e85cc4438f11f317f65458105be00feeba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345337477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b19a7e19813d6639c28cd1bb2a54a091ce21cec682d290dc1a65e5318392cc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:27:36 GMT
ADD file:b2f28be97ca37b14e2019f30dd74a37bf96501fa17ff3dc7780484ef9719f706 in / 
# Wed, 12 Apr 2023 00:27:37 GMT
CMD ["/bin/bash"]
# Wed, 12 Apr 2023 11:07:44 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 12 Apr 2023 11:07:45 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Wed, 12 Apr 2023 11:07:45 GMT
ENV PS_VERSION=8.0.32-24.1
# Wed, 12 Apr 2023 11:07:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1
# Wed, 12 Apr 2023 11:07:45 GMT
ENV OS_VER=el9
# Wed, 12 Apr 2023 11:07:45 GMT
ENV FULL_PERCONA_VERSION=8.0.32-24.1.el9
# Wed, 12 Apr 2023 11:07:45 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.32-1.el9
# Wed, 12 Apr 2023 11:07:45 GMT
ENV PS_REPO=testing
# Wed, 12 Apr 2023 11:07:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Wed, 12 Apr 2023 11:08:31 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Wed, 12 Apr 2023 11:08:34 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Wed, 12 Apr 2023 11:08:34 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Wed, 12 Apr 2023 11:08:34 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Wed, 12 Apr 2023 11:08:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 11:08:35 GMT
USER mysql
# Wed, 12 Apr 2023 11:08:35 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 11:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:649c808906367be985ea3113884c0bde32abcb2dde0a21490c8d6ed08d072dfd`  
		Last Modified: Wed, 12 Apr 2023 00:28:27 GMT  
		Size: 88.6 MB (88588804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f2ae2440738c1fbbb1c8e7194ceaaf3f226e127a7109b7e309ba28c16e2a55`  
		Last Modified: Wed, 12 Apr 2023 11:09:09 GMT  
		Size: 1.6 KB (1631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170f341d55ca253e66762b2096902907d34235b51b26a962abad74fe771b816`  
		Last Modified: Wed, 12 Apr 2023 11:09:10 GMT  
		Size: 7.4 MB (7373771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3fd55d475505da91f29a79a6b29c0db5702a2feca64842995a7c2a534461061`  
		Last Modified: Wed, 12 Apr 2023 11:09:41 GMT  
		Size: 249.4 MB (249369020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5d3fe0731099c15930b7a635456929809a9ec9fc5e737ebd2e90bc9bb88427`  
		Last Modified: Wed, 12 Apr 2023 11:09:09 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc53e1746d614549efc163acfdc8c4ce436febeaa19f14f7bf25a45482facbc5`  
		Last Modified: Wed, 12 Apr 2023 11:09:09 GMT  
		Size: 3.1 KB (3090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
