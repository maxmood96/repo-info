## `mysql:lts`

```console
$ docker pull mysql@sha256:ed913e1525aa6a8921f7bbfa1f0e427624479007d2546d7c3ae4717f293fb2bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:bd0123dddb3c074d7fe94fabd6f589b00d55d0b63a73928045edfcae361d99be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169775176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff286469c4ab2001eb620d63bc871ef57ef9743353a5c8d8c8e2c65fdfa48899`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d8a38112d165940510d5cfd57f316139caf4069546c97dfc10a08f33f3f1ca9f in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12d7e45337f84111b352ed27b6a21ab109dec7571b23ebc522b6bb6b318d883b`  
		Last Modified: Mon, 09 Sep 2024 22:21:36 GMT  
		Size: 49.2 MB (49237791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a626b1be06b99d2afe0fbca3876bd1fa9000ab246ea8ede4345c600d048115b`  
		Last Modified: Mon, 09 Sep 2024 23:02:19 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae8850769f9d5d0f9c6a4a6d1418e833ca3beeda167969308f9da75ffe7505e`  
		Last Modified: Mon, 09 Sep 2024 23:02:19 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baeb5d4fd82073d687687766055816f2dc2412cf0813f4742175a86fc81901e`  
		Last Modified: Mon, 09 Sep 2024 23:02:19 GMT  
		Size: 6.7 MB (6735197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe31d8e26ccf043b3178060df90b71a46040d36c4d135ff7f7c134c20aa48e1`  
		Last Modified: Mon, 09 Sep 2024 23:02:19 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57091c30a083b94531719ac5b4083186d3a78f182bfba8b7dfd94c4fe8b4216`  
		Last Modified: Mon, 09 Sep 2024 23:02:20 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda4cac09bbad7a07f0c89259b9650bf1849a8fe8cea9c1e915b904401572e16`  
		Last Modified: Mon, 09 Sep 2024 23:02:21 GMT  
		Size: 47.2 MB (47249499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ec65ca0199b6ac97a9977a03994d0ffde2455b7a1cd880619ef3c782d65c7e`  
		Last Modified: Mon, 09 Sep 2024 23:02:20 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eefccfc825029d07451b158f792577c7a27d146227226ea2688ec0d5c027491`  
		Last Modified: Mon, 09 Sep 2024 23:02:21 GMT  
		Size: 65.6 MB (65560218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a9254e9d7d8c584c656d6c2c0d16e25efc82d8f36a35f6ff2f1cdcf5203f6b`  
		Last Modified: Mon, 09 Sep 2024 23:02:21 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:c767de0a3b58705c5efa7a91ae3abb090a8c9dc9908b8d478a551bc1144c3d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a86a1de12a3e7a2a8c6a55a38a494afff5511cc7ca7102818223091db83f968`

```dockerfile
```

-	Layers:
	-	`sha256:31513323e6ff552f9f80f68ef5924348cb9e8894f77d8d8aa0e6d2fab37106f1`  
		Last Modified: Mon, 09 Sep 2024 23:02:19 GMT  
		Size: 13.9 MB (13915240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9a5bdc4d0f0edb1d5d81d8ed06d57b9a11d555a4d694fd56cb42f9e7f49d97`  
		Last Modified: Mon, 09 Sep 2024 23:02:19 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json
