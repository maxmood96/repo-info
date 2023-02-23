## `mysql:latest`

```console
$ docker pull mysql@sha256:4a6a070353dbed7aba8bda3957a82b0c146b10ea58c729908139b9a95025d896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:db0d21b5467c8965f988a8c83cb8da5ef9cabbffe71e58df5146ca0d338a8f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152704350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471a1d4e2ab394ee2dedad7f7af5f35bf24385c0d83d09efbed1e1bd67ab373b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:08:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:08:10 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:08:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:08:39 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:08:40 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:08:40 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:08:41 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:09:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:09:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:09:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:09:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:09:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:09:48 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:09:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:09:48 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:09:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba988bb8170fb49396535e5f0341ae56a3cdb8a622efe05b75739c13e0a27`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec3cfb3fc9bbac5a7fad279c895a4989a784dbdcc69d18db0e8a47681df6db`  
		Last Modified: Thu, 23 Feb 2023 20:10:33 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dc4af73e87601565a6cd2181eec316f8bf4120fba26b25a8dfc0078e94e533`  
		Last Modified: Thu, 23 Feb 2023 20:10:32 GMT  
		Size: 4.6 MB (4613213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a350ad9c086a116479936c84bff4dfc7156ff44a93a73bfa6cadd5b9f1edee43`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a3c5c87d3c640f79c72bdfda49423da306d4fc4b3ca3f8103472699f18e3a8`  
		Last Modified: Thu, 23 Feb 2023 20:10:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979a0c1eab55d6b996370483dc83eac9caa6203a1be61910f5ea2765bff9d1`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 56.2 MB (56207236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110576fdf45727b9217d3285beccb29918496ae0bba0f25b88c2f4386f66944`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cdf87e862c39a3bc009ed0bc9a7dcc4e4f2f24c7ee9954273cf9715706bfb`  
		Last Modified: Thu, 23 Feb 2023 20:10:38 GMT  
		Size: 46.3 MB (46338958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c417f0887b0e51dab2ec9fedf0455399cf93ad64cfb80cebe8bb5db900967a36`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53b31fb932ebd2336b9dbd2489c4305c1f332ae631c659aaa23954fbee9aa59`  
		Last Modified: Thu, 23 Feb 2023 20:10:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3a45bb7a17ade719e02f5ce8e6aed5ce21a2f09abde4d2c97d9ae53226be2598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56abd784e5d20b4a9bc40868b39ead0d190a354cfa1ceec3236bc61e46014c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Feb 2023 19:52:36 GMT
ADD file:650f46a4a6a15a9b2d6f048bb51976942936d0c5daba7b0337bceacbc4efcf85 in / 
# Thu, 23 Feb 2023 19:52:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 20:10:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 23 Feb 2023 20:10:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 23 Feb 2023 20:10:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Feb 2023 20:11:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 23 Feb 2023 20:11:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Feb 2023 20:11:16 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:11:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 23 Feb 2023 20:11:46 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 23 Feb 2023 20:11:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 23 Feb 2023 20:11:48 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 23 Feb 2023 20:12:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 23 Feb 2023 20:12:20 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Feb 2023 20:12:20 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 23 Feb 2023 20:12:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Feb 2023 20:12:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Feb 2023 20:12:20 GMT
EXPOSE 3306 33060
# Thu, 23 Feb 2023 20:12:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7166504978b203e953381fdfe4d9e7656565d62a75183fcc5bf460e6135e033d`  
		Last Modified: Thu, 23 Feb 2023 19:53:23 GMT  
		Size: 43.5 MB (43459902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1bfc60852ffa4fdae0e5ec4d962d8bada8c2924866b863514409a7ab19045a`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9743ce35739f0135e234cfeff32a184fa37af2de11e9e26e7505b6a5c81dde9`  
		Last Modified: Thu, 23 Feb 2023 20:12:51 GMT  
		Size: 913.0 KB (912996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d90c3aba8b80c4fd637085a4a682237b93fde3f3fedd20ff459d9b1a9614486`  
		Last Modified: Thu, 23 Feb 2023 20:12:50 GMT  
		Size: 4.5 MB (4459446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82617eb68fb5da3a372a3eca5c8156cd1bb1910d886a32c3d7fddf4bea9c17dd`  
		Last Modified: Thu, 23 Feb 2023 20:12:49 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15220bd69b79d585be35ae5b947548c3db2c0b0ea643a46c25cbf061b9b6a6`  
		Last Modified: Thu, 23 Feb 2023 20:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75486e482b1226f7ee00d91bc04420f441778b21dc17606cf4e34e6e699d4f69`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 55.6 MB (55612433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f208ca0933b830a7ea9fd2c4fdddd6f5e2993109308e7335b2cbb188ad034b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24442b23deeaa2d3905d4e83d84db883d64be63d6cc791a42f67a19f28c67032`  
		Last Modified: Thu, 23 Feb 2023 20:12:53 GMT  
		Size: 47.2 MB (47158659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c900f20367eaf7cd229eaf8700c11fec28409e7267d2cad034efeb45c493b`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc4e3659e2054f7b8a4ddf404adc0af1066666ec3ca30c25914e26d00e8a1c5`  
		Last Modified: Thu, 23 Feb 2023 20:12:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
