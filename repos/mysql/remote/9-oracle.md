## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:f0ef1d92fa650fcfa5b85f1d82bb1a56a6dd579bf256b8f8f2a5a0b1b61c8b0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6e5e46e6aece0bc8edb5abecc6fd726653f36447860f7f4dbf3481c91b477f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273466268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0546e1d5d69deeb824bd3e73e04986f5b4db42ec803d0d3ca3b290f3affb0f93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:10:31 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 05 May 2026 23:10:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 05 May 2026 23:10:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 05 May 2026 23:11:01 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:11:02 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 05 May 2026 23:11:02 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 05 May 2026 23:11:02 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 05 May 2026 23:11:02 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 05 May 2026 23:11:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 05 May 2026 23:11:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 05 May 2026 23:11:33 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 05 May 2026 23:12:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 05 May 2026 23:12:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 May 2026 23:12:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:12:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:12:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 05 May 2026 23:12:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa99ae45fefb5f6a7ed50275e70e3f3714cf18770bda745aaa36de68c41696e`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2289aa81323e2b0090f4c13bf53064c99a823e425b4fe2cc05dd8e6c1b0c96d9`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad527af331bd940f9dfe23a1e2bb9ed82b3f34e6b7ce578e228c7a9e387142`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 6.2 MB (6173037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98aef952816f0b6673e8b353cfd745d5711c61474abaf2af0efeb19f92b801fc`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1e11de502d217dc61c5400a0bb6489836e8f4ef60dcfb9e9d62720d40247cd`  
		Last Modified: Tue, 05 May 2026 23:12:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e070bfedbe5ce6c72ad186420e9e3cbc5945d8731c9c8c03a1a0d85248a7597a`  
		Last Modified: Tue, 05 May 2026 23:12:55 GMT  
		Size: 57.0 MB (56974048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18084fb5d973ffa469e26481d2e5f67d51ad04495181e2e18e7ab2ca0f123f61`  
		Last Modified: Tue, 05 May 2026 23:12:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2253d147eadeb685bf8a642fc68fc1fe7d9b5442d69878282f4db87518633e`  
		Last Modified: Tue, 05 May 2026 23:12:58 GMT  
		Size: 162.2 MB (162216397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53faec57e67345baf7d6995958367b09f5d10ad70f0cf8a0971c672bb9d5a0d6`  
		Last Modified: Tue, 05 May 2026 23:12:54 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5372a010632594e58ce3fc64b3b17aae339dc0c17471ee0bad296aca8bc6ec83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c17f0dd74f710db7e1e919bc6d93f437bfb1c95ca5b52cdf95376b0a6bc34d7`

```dockerfile
```

-	Layers:
	-	`sha256:88f318259e725efbac326e246d08c1cb1930e6c9e53803e74323834c3ae14f69`  
		Last Modified: Tue, 05 May 2026 23:12:53 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3769042852bceaeb1ac5070230220f4d92bae767104f79b3da78713e1a05b98c`  
		Last Modified: Tue, 05 May 2026 23:12:52 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:fe2ab593dcd36d9d22870c101abfcf43fda63f7cde1a91a0db09a8cc5a16195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269903259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0573f2dfde97b7842b655c77d5605174ffc81a85ef53af603b655b852f158889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2026 23:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 05 May 2026 23:10:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 05 May 2026 23:10:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 05 May 2026 23:10:48 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 05 May 2026 23:10:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 05 May 2026 23:10:49 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 05 May 2026 23:10:49 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 05 May 2026 23:10:49 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 05 May 2026 23:11:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 05 May 2026 23:11:21 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 05 May 2026 23:11:21 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 05 May 2026 23:12:07 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 05 May 2026 23:12:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 May 2026 23:12:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:12:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:12:07 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 05 May 2026 23:12:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d0078524b97ea969c6c667b5939d98e9a566271865200b8c500dcf4db0537`  
		Last Modified: Tue, 05 May 2026 23:12:43 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5818494ab9c6dc61c3510a69bf6aac005bb961d9abcec45739be2dd3366025`  
		Last Modified: Tue, 05 May 2026 23:12:43 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d0d92b0e4bfd5dd98efab07720fa79751381dc1bc23e5751646db54a6995ce`  
		Last Modified: Tue, 05 May 2026 23:12:43 GMT  
		Size: 5.8 MB (5790698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70c6f3cf7aeece63955cc06a069758955d7bfeedfde93125e34c55fe9da88d0`  
		Last Modified: Tue, 05 May 2026 23:12:43 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ea208aed85c8285d45f3a5e3079348a2f415d3b92be51230fb3f56ff2f47f9`  
		Last Modified: Tue, 05 May 2026 23:12:44 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f25e1b78a0b70ec89c919237502c2dd8ade455ca03cdb7fe2d6dbc9598df9db`  
		Last Modified: Tue, 05 May 2026 23:12:46 GMT  
		Size: 57.0 MB (56982715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c4982b274c2fe4b8377b0aac4f1a6877783765341b38714ad0b229a08d6fd`  
		Last Modified: Tue, 05 May 2026 23:12:44 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b4df0b1a9322da3c1f986976a96053756e8216c6c95f577f13f865276fd542`  
		Last Modified: Tue, 05 May 2026 23:12:49 GMT  
		Size: 160.5 MB (160484030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995635aed67e79dfcd73ce3f49084b2c305024665ef4af1bf0fe975ea72f5b7a`  
		Last Modified: Tue, 05 May 2026 23:12:45 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b92f95c38479ba63b26527a3e091e38308cf1d61b2b9bea8da2c44dda368184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fdc720f93fb6b517cfd4a5b3e405dfb1215503c814c57eb240439ae8095f72`

```dockerfile
```

-	Layers:
	-	`sha256:2962f277ff152b5c0ba0d4efd9bd5dc3a0a138bf38748cd1cf02283b4d50e119`  
		Last Modified: Tue, 05 May 2026 23:12:43 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c24e13ebf10a6c3503c613d72eb20769cf8ac3438e55e2b89d657adc1a102b`  
		Last Modified: Tue, 05 May 2026 23:12:43 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json
