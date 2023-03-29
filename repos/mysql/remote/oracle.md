## `mysql:oracle`

```console
$ docker pull mysql@sha256:e8dc80474af00e0c49d55742815da52073f466059648738e648c9dd262ff51db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:16495103f160c1c1cc3fb608fc06bc189d47150f0f5ed6734c5fbd1d0a1fbf16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156545941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7ac5436057ed32e37404358d126fe9ab7b2b4e99906eaad0eed6af8e04921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:42:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:42:04 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:42:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:42:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:42:32 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:42:32 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:42:33 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:42:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:43:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:43:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:43:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:43:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:43:40 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:43:40 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:43:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:43:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:43:41 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:43:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1ebcf71068d314e294975f852d15ac218c37896c5e23ae3e39f5092c1768a7`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae5de5bc10fdeea5d37536ee6cf2f41e0908fa73f9d9d060f7d527464be9c9f`  
		Last Modified: Wed, 29 Mar 2023 00:45:23 GMT  
		Size: 982.8 KB (982821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be806b053349f89652c04de98825ac2445685060c21c9c7db3527ab8da17bb`  
		Last Modified: Wed, 29 Mar 2023 00:45:22 GMT  
		Size: 4.6 MB (4612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe4db00091d4a386853badc31289b986611a1e9d38d5eb1bd4d0e2268ded65c`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc80326f5beb88897a02c7b576f49d75384ce29af4b1c7c93c5c1abc8b8e0c7`  
		Last Modified: Wed, 29 Mar 2023 00:45:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8b64cd8427351aa7054abcbba40d2a0f53deaec74044e2f19ecd292727916e`  
		Last Modified: Wed, 29 Mar 2023 00:45:27 GMT  
		Size: 56.2 MB (56206507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6175ffbdd8248d25856ba2d3b70018c0525fae4d9be288cb840468fab9418828`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2321d401545366afcf21ce562c041687d498f03823e250402b5bf94606e10c24`  
		Last Modified: Wed, 29 Mar 2023 00:45:28 GMT  
		Size: 50.2 MB (50172690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fea5c11a8052a03559a2a7ce0ed313acb0e2be46212fb9c9fe632c70ffb25a`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe213e7bfd3398acb82a779b3d17f35cf3e208d0fe23619bfb7b931ec1137df`  
		Last Modified: Wed, 29 Mar 2023 00:45:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a4deb601ab9761ff3edaabd920d329e0e7211967dc10f6efabd7d8cf1f725ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555c2c40b6822b293d86d48dbf26d6343fee16b248cd12e33b61a1a2c77fd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:57:07 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 29 Mar 2023 00:57:07 GMT
ENV GOSU_VERSION=1.16
# Wed, 29 Mar 2023 00:57:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 29 Mar 2023 00:57:35 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:57:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 29 Mar 2023 00:57:36 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:57:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 29 Mar 2023 00:58:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 29 Mar 2023 00:58:05 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 29 Mar 2023 00:58:05 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 29 Mar 2023 00:58:34 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 29 Mar 2023 00:58:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 29 Mar 2023 00:58:36 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 29 Mar 2023 00:58:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 29 Mar 2023 00:58:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 00:58:37 GMT
EXPOSE 3306 33060
# Wed, 29 Mar 2023 00:58:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5489cd119922be14437e6bd6a72ded4b4d61aee8e508ef8f42e20a32287bc8`  
		Last Modified: Wed, 29 Mar 2023 00:58:54 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548de0f50a694ff391fafc42f9fdfc6c8704608980aef09bc5b9aff186f740ab`  
		Last Modified: Wed, 29 Mar 2023 00:58:55 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecb4ab1b60e2172f1ef6dc97fd4c1b6ce00be4f154597edf3dc7abe7cddf8f2`  
		Last Modified: Wed, 29 Mar 2023 00:58:53 GMT  
		Size: 4.5 MB (4465557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6647ae2869c9043c7eed3d0961b46a5de2e63d0d23b0a7a8f3f7e943376e1`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2540ff01e7afd5eb538dceea1d6d4dc604d6b6c351dc54a6df327fa779428ce`  
		Last Modified: Wed, 29 Mar 2023 00:58:52 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54491c0d0f1a190cdce2f06d8938af727c99bff1501cb57d1496d1f669876f24`  
		Last Modified: Wed, 29 Mar 2023 00:58:57 GMT  
		Size: 55.6 MB (55605395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c90bf26af9397ed1307378a35f4b7eeda3cbcf5fb63e99b48ad706c68f29c`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e81bb3be76ca86e61ae0cdce33411e09214c860f0c2aeb28615f22d039b90`  
		Last Modified: Wed, 29 Mar 2023 00:58:58 GMT  
		Size: 51.0 MB (50999074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead66f33bf9ff133541709bf10458449891a0f75b9d4c9940377e326b4e3430`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccd3492e952d2e2d82b23a2f610220c7b3329532cdf0581a1bb2f9ec75e63a`  
		Last Modified: Wed, 29 Mar 2023 00:58:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
