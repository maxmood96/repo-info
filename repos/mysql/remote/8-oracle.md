## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:d6164ff4855b9b3f2c7748c6ec564ccff841f79a7023db0f9293143481a44b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:13e429971e970ebcb7bc611de52d71a3c444247dc67cf7475a02718f6a5ef559
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165661773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05db07cd74c0520c8ffe5f7638063719a886f9115cecacc0654d981caf5d27f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 May 2023 21:20:28 GMT
ADD file:e15c235506d8dd134e69d458a7c0afefef1522e9d0cfb28e3538760ddf032785 in / 
# Wed, 24 May 2023 21:20:29 GMT
CMD ["/bin/bash"]
# Wed, 24 May 2023 21:41:30 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 24 May 2023 21:41:30 GMT
ENV GOSU_VERSION=1.16
# Wed, 24 May 2023 21:41:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 May 2023 21:42:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 24 May 2023 21:42:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 24 May 2023 21:42:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 May 2023 21:42:01 GMT
ENV MYSQL_VERSION=8.0.33-1.el8
# Wed, 24 May 2023 21:42:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 24 May 2023 21:42:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 24 May 2023 21:42:34 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 24 May 2023 21:42:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1.el8
# Wed, 24 May 2023 21:43:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 24 May 2023 21:43:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 May 2023 21:43:12 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 24 May 2023 21:43:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 24 May 2023 21:43:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 21:43:13 GMT
EXPOSE 3306 33060
# Wed, 24 May 2023 21:43:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:90e2fb2facff1c5093f0ebfa9d08fde487930822d9ac278bb2df0195610f1d13`  
		Last Modified: Wed, 24 May 2023 21:21:24 GMT  
		Size: 44.9 MB (44873648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba60eb20fd5f1585d3f8555cd5f6c77ce046c2dba0065b2fe1efc2143594c731`  
		Last Modified: Wed, 24 May 2023 21:43:43 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f509402d4698ff849d46bd38250cea5958a084f3c041f09b6709aed5490d6f0`  
		Last Modified: Wed, 24 May 2023 21:43:44 GMT  
		Size: 982.8 KB (982822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496c2cfa6815431e3a274125695fdfa32f8f79e4ce06f8813f567e95e3b88b9d`  
		Last Modified: Wed, 24 May 2023 21:43:42 GMT  
		Size: 4.6 MB (4614833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec1dfa9522c3018cc0fd55036bd8bda764284ed6e6dbbce58ad56546c7063e5`  
		Last Modified: Wed, 24 May 2023 21:43:41 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dec7ba896f8a2aba8593161fbbdabcdb3084d2a32d205e74adea0512221d1ad`  
		Last Modified: Wed, 24 May 2023 21:43:41 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9ff75362b09bf9dd347c0f401765f321ad4703899afcc942a95b3fcd05b2a4`  
		Last Modified: Wed, 24 May 2023 21:43:47 GMT  
		Size: 58.6 MB (58612867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e4682f90146968127641c6e2e684397e16b0fa1c359f5044495d32af83a8ce`  
		Last Modified: Wed, 24 May 2023 21:43:39 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffdeecd6fb69ba22d67316deb7cdad5ff8c7ef16192ac8612a43ca356092038`  
		Last Modified: Wed, 24 May 2023 21:43:49 GMT  
		Size: 56.6 MB (56567927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4346ccfb53fc40d40662c29efd36b162063090bde8ce918879ffc8031eb85df`  
		Last Modified: Wed, 24 May 2023 21:43:39 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434c13bc32de0d05d006b05823d477cc03cd9f9eff367e6e6ee6b5a2810774c3`  
		Last Modified: Wed, 24 May 2023 21:43:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7f6dd9cce985f7d4037f3ac8f08f7c427313f7428f524fbed6b8631d599dd036
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170099508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe893ca746498cfd79df295cdce9199635e9d572805e85f36293170323f5ebdb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 May 2023 21:44:09 GMT
ADD file:8c6f57a98019c407c59b2adbf7da54536eff3a7ca62c46883bbc60975b39ad04 in / 
# Wed, 24 May 2023 21:44:09 GMT
CMD ["/bin/bash"]
# Wed, 24 May 2023 22:00:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 24 May 2023 22:00:17 GMT
ENV GOSU_VERSION=1.16
# Wed, 24 May 2023 22:00:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 May 2023 22:00:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 24 May 2023 22:00:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 24 May 2023 22:00:46 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 May 2023 22:00:46 GMT
ENV MYSQL_VERSION=8.0.33-1.el8
# Wed, 24 May 2023 22:00:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 24 May 2023 22:01:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 24 May 2023 22:01:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 24 May 2023 22:01:17 GMT
ENV MYSQL_SHELL_VERSION=8.0.33-1.el8
# Wed, 24 May 2023 22:01:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 24 May 2023 22:01:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 May 2023 22:01:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 24 May 2023 22:01:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 24 May 2023 22:01:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 22:01:54 GMT
EXPOSE 3306 33060
# Wed, 24 May 2023 22:01:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0bb308beee4aa3eb768d546b1ee61303d6f190f63bed75dc7f88ecc26018a944`  
		Last Modified: Wed, 24 May 2023 21:44:58 GMT  
		Size: 43.8 MB (43791991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bdb7032bf305a3cccbf8a5a87199949fb2d7111acc441bf138ec1d8da4b9cf`  
		Last Modified: Wed, 24 May 2023 22:02:19 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c141ac75efa380ab407b0e332507e70e28734b3c4a4452130c89844326111060`  
		Last Modified: Wed, 24 May 2023 22:02:19 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67614e9d4dc3ab5c980e6816387361cc22f6d0e49baf2881db146d0c537fc867`  
		Last Modified: Wed, 24 May 2023 22:02:18 GMT  
		Size: 4.5 MB (4452975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3ae2d7489458f2fa86a134fa7882e4a295fb503e3a76902038aed8714fc5d7`  
		Last Modified: Wed, 24 May 2023 22:02:17 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9fe26631bb3ff3b2ee24ffd5d0d18a78c57828273707aa7d7264225e44be74`  
		Last Modified: Wed, 24 May 2023 22:02:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956edc6a4dee11e74064920fe96dbdf6a2ba977a800e158f0f8a0c47ffe57e19`  
		Last Modified: Wed, 24 May 2023 22:02:21 GMT  
		Size: 57.9 MB (57872924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2b9f819df46484e9a57571809d3f466eb30fd9983c710ed0e76fb6a062df25`  
		Last Modified: Wed, 24 May 2023 22:02:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea676d6c3a502eb9361c0a4a756d509a9c369956fae4c1824d0b111875221198`  
		Last Modified: Wed, 24 May 2023 22:02:23 GMT  
		Size: 63.1 MB (63058937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83456db5aaf77ca573b2c0081dc45c73d338e96dfc0e7b9a35c65ddcca2451eb`  
		Last Modified: Wed, 24 May 2023 22:02:15 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56bb6ffc164d00b09844a1f9fe7892a03baeccb3c382ce825d8e18906b2be9`  
		Last Modified: Wed, 24 May 2023 22:02:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
