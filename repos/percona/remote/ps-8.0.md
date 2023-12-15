## `percona:ps-8.0`

```console
$ docker pull percona@sha256:8827ca9c243dc75740753de097f72a1ae423e5dffa03a7800ee6fba88c4ccfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:93e573e30d312666e8f24a718c25a369b07c427d2b04e07b78516c0e5784dfad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393837670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48376ce72d696b0936ce19a7a9188bb1aed50cdf31efe8bd54b3e715fbae3479`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 14 Dec 2023 23:20:45 GMT
ADD file:e3a43112d59c4c8299261c1c569182422dc81858961eab4a268745a5013067a0 in / 
# Thu, 14 Dec 2023 23:20:46 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:38:54 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 14 Dec 2023 23:38:54 GMT
RUN set -ex;     groupdel input;     userdel systemd-coredump;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql
# Thu, 14 Dec 2023 23:38:54 GMT
ENV PS_VERSION=8.0.34-26.1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.34-1
# Thu, 14 Dec 2023 23:38:55 GMT
ENV OS_VER=el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_PERCONA_VERSION=8.0.34-26.1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.34-1.el9
# Thu, 14 Dec 2023 23:38:55 GMT
ENV PS_REPO=release
# Thu, 14 Dec 2023 23:38:58 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO}
# Thu, 14 Dec 2023 23:39:58 GMT
RUN set -ex;     dnf -y install epel-release;     rpm -e --nodeps tzdata;     dnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;         dnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql
# Thu, 14 Dec 2023 23:40:02 GMT
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Thu, 14 Dec 2023 23:40:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 14 Dec 2023 23:40:03 GMT
COPY file:8e394b40e5593ab1fb7ffd68ce2a3169f41e4e257f96ad515f6af4567362a3c5 in /docker-entrypoint.sh 
# Thu, 14 Dec 2023 23:40:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Dec 2023 23:40:03 GMT
USER mysql
# Thu, 14 Dec 2023 23:40:03 GMT
EXPOSE 3306 33060
# Thu, 14 Dec 2023 23:40:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:03b80e2bc55d10b85408f5a3ba7f319b819881e7ef9325222577bc17848da474`  
		Last Modified: Thu, 14 Dec 2023 23:22:23 GMT  
		Size: 94.3 MB (94346229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1164c810d59cbe4d0034b80940aa47b51e892e893598481514053a66ab8a4a`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee069b0554ed69fa0114c5c4d5a87c8b99537084fb6998f32ee544074d873c6c`  
		Last Modified: Thu, 14 Dec 2023 23:40:49 GMT  
		Size: 7.3 MB (7292863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646d131413d934d13704278a4af16be2ac19b082fa3859e31e5e60f1e0052a1d`  
		Last Modified: Thu, 14 Dec 2023 23:41:31 GMT  
		Size: 292.2 MB (292192702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc37b9aa76e2f409a6d9cf73e492f00bf58466f13eb62831aadf134212c602`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f915fe3e2fa58407938b0c1736de69fba59bb0c920a37aa876c72b9cd4ca6f3`  
		Last Modified: Thu, 14 Dec 2023 23:40:48 GMT  
		Size: 3.1 KB (3091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
