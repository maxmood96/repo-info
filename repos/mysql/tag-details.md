<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux8`](#mysql8-oraclelinux8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bullseye`](#mysql80-bullseye)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux8`](#mysql80-oraclelinux8)
-	[`mysql:8.0.36`](#mysql8036)
-	[`mysql:8.0.36-bullseye`](#mysql8036-bullseye)
-	[`mysql:8.0.36-debian`](#mysql8036-debian)
-	[`mysql:8.0.36-oracle`](#mysql8036-oracle)
-	[`mysql:8.0.36-oraclelinux8`](#mysql8036-oraclelinux8)
-	[`mysql:8.3`](#mysql83)
-	[`mysql:8.3-oracle`](#mysql83-oracle)
-	[`mysql:8.3-oraclelinux8`](#mysql83-oraclelinux8)
-	[`mysql:8.3.0`](#mysql830)
-	[`mysql:8.3.0-oracle`](#mysql830-oracle)
-	[`mysql:8.3.0-oraclelinux8`](#mysql830-oraclelinux8)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux8`](#mysqlinnovation-oraclelinux8)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux8`](#mysqloraclelinux8)

## `mysql:8`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux8`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:3f75dccd64fffa40a06a4a9256206280a5ddc3e26dea3f1ab0df35b2cc12f472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:094a1638b290a1c5d5faa3f06ac2e3ed975947594db4a60aadc58a92e3d0820b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174711701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6188b3dc37c427f01aac2e8fc2b153044f2861becb8fd0f402bcabb429d71c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e714ea5470c150d90ee69da1f028674313e515f5b3c54fe94e3896b3aa5524`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ada0981f60fda3708effe5ca1e896bd17b0e307b951d76696b8d6cad59466`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae11d1b9d69faaee9664ecf939a2c7fc88ed73d135269e353163b39934f4876`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 4.6 MB (4590811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9be74ddc84185eafd024e29063043eee015ec174ac612c1250d3d7ebe47b44`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a59c7182522928e2dc091099a5f00ac4d95cbfa080182995eb8175bc35854d`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42afee6c9cb6ee9efac8fb6bf9505d3d3c42fd6ea8ef12007237f7946777b9`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 58.5 MB (58506468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1f586b2e2abf128a177a2e00b54fecbaca5eb23a9c6b6e8a29bffb6527f6a`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210e58b61fa3726a89826dcbcd43a93e07c6ae9b8257082c1d15e89b878b05fd`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 59.3 MB (59300444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9719ad703de58410c05950e5f3b8d291ab3dce45ab456dcf1fbe3e1f232105f`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef92b20c8ec10ade9d1228ef999a5ff3afd443bea12717145c725d96c41e6d1`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:8540b9c4cc8b6176af7013e47d420475cbb11377db6f209ebb8f4fd6f7b8e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7b68aa9d27289d647980a35d50f6b331fddb6e074ad05d65c348d076bbf97a`

```dockerfile
```

-	Layers:
	-	`sha256:864b84a5a9c97ee3b88f35bfa7242eecb3f4e13fa57d186c6f4006e317b546e4`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 12.1 MB (12127343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4792e46ce9509aea17bf39c44c30177fc1bc7feb00be1c267c9728b2ae929faf`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c6a27a7f19e497f3ae4c305466d97c7addcad4e4e13ff5a37e4ef27fa4f5eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178480867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e203202cb04420ea6d2723bc9bcab569484343079a91b9d57e996b3d2ae2305`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ca054b36e90122d41f319ab5b71780b711822ba16af311b26f4f986d24a4b7`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f8b126f56cfb316fdab75a02dbdc488ff15690439dee31a49c6485cae86a8d`  
		Last Modified: Fri, 19 Jan 2024 04:24:53 GMT  
		Size: 57.6 MB (57586943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c1d8d06015bc4ec98e98fe5803520279b807a91b9847e4780bb0adff1b3746`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e3c866daa9dfb801fec62fa08488079c59321ea36fab7b120e8f02599a3d3c`  
		Last Modified: Fri, 19 Jan 2024 04:24:54 GMT  
		Size: 65.6 MB (65587915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3376a0ffe43b2fdfc0816d7327d6544d7f6263cb27a6d8a6466a908fe8eba10`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3493b22e2fd94b3a4ed259d3dd726a60b259b9a6067cc2ad27680fd4697f01`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:0c8133bd5b9a43a416ab6809e959165556abd31a4dbf7f9b33bc84a6df72a8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12160665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3064fe20a1d0c80ee2c5f6a6def84dd702ce018e4949838dfe0c5fd2da1a14fe`

```dockerfile
```

-	Layers:
	-	`sha256:697a100cbfed71c0bb43e18be9dbbbff5a24d9b6cb8a2ac6e364b50bab70af0b`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 12.1 MB (12125923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5931c8cd77e08f878390bb365588dc7c4a80febfb2367415415f8e5a1f107da5`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bullseye`

```console
$ docker pull mysql@sha256:26340f6de6eef7560ff5be717a044d818906e236a99ac344603785f70b5d6269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bullseye` - linux; amd64

```console
$ docker pull mysql@sha256:c8ee75a32bfb7395c1c897d3c1889dfc2c974e99052cf68cc3c44577d4bc408e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179126921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fc62e0fca157ac0dc166c14e99d1fde95378349f1ed8e63e112a6b35a10bcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1debian11
# Thu, 18 Jan 2024 17:37:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0194d1cb63034c9bdbaa3df0c1b9d193d5ccb66b1d9b216ab46c95127647749`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ade69351f1fafe41a5ea5dbe4ec23cb4e702bb74f6f0d73d6cc12447972e79`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 4.2 MB (4207452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ef08ebf2f75e85ee5250536ee79f02c17debc80b8845d83e4fc51e920473d`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 1.5 MB (1472443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cceae24050afc033cd7605b596b43072b045b77b94f06fce705296f4b20515`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3d460e6d3f8ed993823b7bc469bd4744f56dff99df1692851d15280a1e0eb0`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 12.5 MB (12454332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113c34d227c93c29f8daa413dd4e7c88a3066d54cfb4719cc7632be952ce0b5b`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ae7eb47461cebdad48ee59bc5e8a7dada3ff578f74417fcacd741df1816c0`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816086d31d6994c1a497efd3c0b7d288de26e365e0a92c53c793966fb42ef32d`  
		Last Modified: Thu, 18 Jan 2024 23:59:16 GMT  
		Size: 129.6 MB (129564091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c63cd51ae7c7f0e9d881fc970c5b8e121606d071ee4b3f20a19ef6f1c6d3aa`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d525e1cf6fab1a8683933c035c7172fee8d20b0215455929bd23243a13e83cb0`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a763557c508841e97a158f398926568c286541275d5cccde1857899bf1e363c4`  
		Last Modified: Thu, 18 Jan 2024 23:59:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bullseye` - unknown; unknown

```console
$ docker pull mysql@sha256:2b88e2680c65055450d6a57cfa3ea40c0ccbc1f87a7be560a2b75c136de0e025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c6e5ad027e3627f0762bee0a62848185d4cc4d250e2de4ff78721141640b26`

```dockerfile
```

-	Layers:
	-	`sha256:326d5dfb36e31ea7aa4e0572384ba5348968e4b223581fe9cb25cc8d8e9bf463`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d99e06c03dbe372a3e70c4ce5aab293a18fd0229d5058f8561283c4e9f14895`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:26340f6de6eef7560ff5be717a044d818906e236a99ac344603785f70b5d6269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c8ee75a32bfb7395c1c897d3c1889dfc2c974e99052cf68cc3c44577d4bc408e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179126921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fc62e0fca157ac0dc166c14e99d1fde95378349f1ed8e63e112a6b35a10bcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1debian11
# Thu, 18 Jan 2024 17:37:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0194d1cb63034c9bdbaa3df0c1b9d193d5ccb66b1d9b216ab46c95127647749`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ade69351f1fafe41a5ea5dbe4ec23cb4e702bb74f6f0d73d6cc12447972e79`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 4.2 MB (4207452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ef08ebf2f75e85ee5250536ee79f02c17debc80b8845d83e4fc51e920473d`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 1.5 MB (1472443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cceae24050afc033cd7605b596b43072b045b77b94f06fce705296f4b20515`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3d460e6d3f8ed993823b7bc469bd4744f56dff99df1692851d15280a1e0eb0`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 12.5 MB (12454332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113c34d227c93c29f8daa413dd4e7c88a3066d54cfb4719cc7632be952ce0b5b`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ae7eb47461cebdad48ee59bc5e8a7dada3ff578f74417fcacd741df1816c0`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816086d31d6994c1a497efd3c0b7d288de26e365e0a92c53c793966fb42ef32d`  
		Last Modified: Thu, 18 Jan 2024 23:59:16 GMT  
		Size: 129.6 MB (129564091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c63cd51ae7c7f0e9d881fc970c5b8e121606d071ee4b3f20a19ef6f1c6d3aa`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d525e1cf6fab1a8683933c035c7172fee8d20b0215455929bd23243a13e83cb0`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a763557c508841e97a158f398926568c286541275d5cccde1857899bf1e363c4`  
		Last Modified: Thu, 18 Jan 2024 23:59:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:2b88e2680c65055450d6a57cfa3ea40c0ccbc1f87a7be560a2b75c136de0e025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c6e5ad027e3627f0762bee0a62848185d4cc4d250e2de4ff78721141640b26`

```dockerfile
```

-	Layers:
	-	`sha256:326d5dfb36e31ea7aa4e0572384ba5348968e4b223581fe9cb25cc8d8e9bf463`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d99e06c03dbe372a3e70c4ce5aab293a18fd0229d5058f8561283c4e9f14895`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:3f75dccd64fffa40a06a4a9256206280a5ddc3e26dea3f1ab0df35b2cc12f472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:094a1638b290a1c5d5faa3f06ac2e3ed975947594db4a60aadc58a92e3d0820b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174711701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6188b3dc37c427f01aac2e8fc2b153044f2861becb8fd0f402bcabb429d71c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e714ea5470c150d90ee69da1f028674313e515f5b3c54fe94e3896b3aa5524`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ada0981f60fda3708effe5ca1e896bd17b0e307b951d76696b8d6cad59466`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae11d1b9d69faaee9664ecf939a2c7fc88ed73d135269e353163b39934f4876`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 4.6 MB (4590811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9be74ddc84185eafd024e29063043eee015ec174ac612c1250d3d7ebe47b44`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a59c7182522928e2dc091099a5f00ac4d95cbfa080182995eb8175bc35854d`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42afee6c9cb6ee9efac8fb6bf9505d3d3c42fd6ea8ef12007237f7946777b9`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 58.5 MB (58506468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1f586b2e2abf128a177a2e00b54fecbaca5eb23a9c6b6e8a29bffb6527f6a`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210e58b61fa3726a89826dcbcd43a93e07c6ae9b8257082c1d15e89b878b05fd`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 59.3 MB (59300444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9719ad703de58410c05950e5f3b8d291ab3dce45ab456dcf1fbe3e1f232105f`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef92b20c8ec10ade9d1228ef999a5ff3afd443bea12717145c725d96c41e6d1`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8540b9c4cc8b6176af7013e47d420475cbb11377db6f209ebb8f4fd6f7b8e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7b68aa9d27289d647980a35d50f6b331fddb6e074ad05d65c348d076bbf97a`

```dockerfile
```

-	Layers:
	-	`sha256:864b84a5a9c97ee3b88f35bfa7242eecb3f4e13fa57d186c6f4006e317b546e4`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 12.1 MB (12127343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4792e46ce9509aea17bf39c44c30177fc1bc7feb00be1c267c9728b2ae929faf`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c6a27a7f19e497f3ae4c305466d97c7addcad4e4e13ff5a37e4ef27fa4f5eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178480867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e203202cb04420ea6d2723bc9bcab569484343079a91b9d57e996b3d2ae2305`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ca054b36e90122d41f319ab5b71780b711822ba16af311b26f4f986d24a4b7`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f8b126f56cfb316fdab75a02dbdc488ff15690439dee31a49c6485cae86a8d`  
		Last Modified: Fri, 19 Jan 2024 04:24:53 GMT  
		Size: 57.6 MB (57586943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c1d8d06015bc4ec98e98fe5803520279b807a91b9847e4780bb0adff1b3746`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e3c866daa9dfb801fec62fa08488079c59321ea36fab7b120e8f02599a3d3c`  
		Last Modified: Fri, 19 Jan 2024 04:24:54 GMT  
		Size: 65.6 MB (65587915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3376a0ffe43b2fdfc0816d7327d6544d7f6263cb27a6d8a6466a908fe8eba10`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3493b22e2fd94b3a4ed259d3dd726a60b259b9a6067cc2ad27680fd4697f01`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0c8133bd5b9a43a416ab6809e959165556abd31a4dbf7f9b33bc84a6df72a8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12160665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3064fe20a1d0c80ee2c5f6a6def84dd702ce018e4949838dfe0c5fd2da1a14fe`

```dockerfile
```

-	Layers:
	-	`sha256:697a100cbfed71c0bb43e18be9dbbbff5a24d9b6cb8a2ac6e364b50bab70af0b`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 12.1 MB (12125923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5931c8cd77e08f878390bb365588dc7c4a80febfb2367415415f8e5a1f107da5`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux8`

```console
$ docker pull mysql@sha256:3f75dccd64fffa40a06a4a9256206280a5ddc3e26dea3f1ab0df35b2cc12f472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:094a1638b290a1c5d5faa3f06ac2e3ed975947594db4a60aadc58a92e3d0820b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174711701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6188b3dc37c427f01aac2e8fc2b153044f2861becb8fd0f402bcabb429d71c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e714ea5470c150d90ee69da1f028674313e515f5b3c54fe94e3896b3aa5524`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ada0981f60fda3708effe5ca1e896bd17b0e307b951d76696b8d6cad59466`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae11d1b9d69faaee9664ecf939a2c7fc88ed73d135269e353163b39934f4876`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 4.6 MB (4590811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9be74ddc84185eafd024e29063043eee015ec174ac612c1250d3d7ebe47b44`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a59c7182522928e2dc091099a5f00ac4d95cbfa080182995eb8175bc35854d`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42afee6c9cb6ee9efac8fb6bf9505d3d3c42fd6ea8ef12007237f7946777b9`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 58.5 MB (58506468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1f586b2e2abf128a177a2e00b54fecbaca5eb23a9c6b6e8a29bffb6527f6a`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210e58b61fa3726a89826dcbcd43a93e07c6ae9b8257082c1d15e89b878b05fd`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 59.3 MB (59300444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9719ad703de58410c05950e5f3b8d291ab3dce45ab456dcf1fbe3e1f232105f`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef92b20c8ec10ade9d1228ef999a5ff3afd443bea12717145c725d96c41e6d1`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:8540b9c4cc8b6176af7013e47d420475cbb11377db6f209ebb8f4fd6f7b8e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7b68aa9d27289d647980a35d50f6b331fddb6e074ad05d65c348d076bbf97a`

```dockerfile
```

-	Layers:
	-	`sha256:864b84a5a9c97ee3b88f35bfa7242eecb3f4e13fa57d186c6f4006e317b546e4`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 12.1 MB (12127343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4792e46ce9509aea17bf39c44c30177fc1bc7feb00be1c267c9728b2ae929faf`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c6a27a7f19e497f3ae4c305466d97c7addcad4e4e13ff5a37e4ef27fa4f5eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178480867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e203202cb04420ea6d2723bc9bcab569484343079a91b9d57e996b3d2ae2305`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ca054b36e90122d41f319ab5b71780b711822ba16af311b26f4f986d24a4b7`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f8b126f56cfb316fdab75a02dbdc488ff15690439dee31a49c6485cae86a8d`  
		Last Modified: Fri, 19 Jan 2024 04:24:53 GMT  
		Size: 57.6 MB (57586943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c1d8d06015bc4ec98e98fe5803520279b807a91b9847e4780bb0adff1b3746`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e3c866daa9dfb801fec62fa08488079c59321ea36fab7b120e8f02599a3d3c`  
		Last Modified: Fri, 19 Jan 2024 04:24:54 GMT  
		Size: 65.6 MB (65587915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3376a0ffe43b2fdfc0816d7327d6544d7f6263cb27a6d8a6466a908fe8eba10`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3493b22e2fd94b3a4ed259d3dd726a60b259b9a6067cc2ad27680fd4697f01`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:0c8133bd5b9a43a416ab6809e959165556abd31a4dbf7f9b33bc84a6df72a8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12160665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3064fe20a1d0c80ee2c5f6a6def84dd702ce018e4949838dfe0c5fd2da1a14fe`

```dockerfile
```

-	Layers:
	-	`sha256:697a100cbfed71c0bb43e18be9dbbbff5a24d9b6cb8a2ac6e364b50bab70af0b`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 12.1 MB (12125923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5931c8cd77e08f878390bb365588dc7c4a80febfb2367415415f8e5a1f107da5`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36`

```console
$ docker pull mysql@sha256:3f75dccd64fffa40a06a4a9256206280a5ddc3e26dea3f1ab0df35b2cc12f472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36` - linux; amd64

```console
$ docker pull mysql@sha256:094a1638b290a1c5d5faa3f06ac2e3ed975947594db4a60aadc58a92e3d0820b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174711701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6188b3dc37c427f01aac2e8fc2b153044f2861becb8fd0f402bcabb429d71c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e714ea5470c150d90ee69da1f028674313e515f5b3c54fe94e3896b3aa5524`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ada0981f60fda3708effe5ca1e896bd17b0e307b951d76696b8d6cad59466`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae11d1b9d69faaee9664ecf939a2c7fc88ed73d135269e353163b39934f4876`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 4.6 MB (4590811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9be74ddc84185eafd024e29063043eee015ec174ac612c1250d3d7ebe47b44`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a59c7182522928e2dc091099a5f00ac4d95cbfa080182995eb8175bc35854d`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42afee6c9cb6ee9efac8fb6bf9505d3d3c42fd6ea8ef12007237f7946777b9`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 58.5 MB (58506468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1f586b2e2abf128a177a2e00b54fecbaca5eb23a9c6b6e8a29bffb6527f6a`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210e58b61fa3726a89826dcbcd43a93e07c6ae9b8257082c1d15e89b878b05fd`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 59.3 MB (59300444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9719ad703de58410c05950e5f3b8d291ab3dce45ab456dcf1fbe3e1f232105f`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef92b20c8ec10ade9d1228ef999a5ff3afd443bea12717145c725d96c41e6d1`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:8540b9c4cc8b6176af7013e47d420475cbb11377db6f209ebb8f4fd6f7b8e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7b68aa9d27289d647980a35d50f6b331fddb6e074ad05d65c348d076bbf97a`

```dockerfile
```

-	Layers:
	-	`sha256:864b84a5a9c97ee3b88f35bfa7242eecb3f4e13fa57d186c6f4006e317b546e4`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 12.1 MB (12127343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4792e46ce9509aea17bf39c44c30177fc1bc7feb00be1c267c9728b2ae929faf`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c6a27a7f19e497f3ae4c305466d97c7addcad4e4e13ff5a37e4ef27fa4f5eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178480867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e203202cb04420ea6d2723bc9bcab569484343079a91b9d57e996b3d2ae2305`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ca054b36e90122d41f319ab5b71780b711822ba16af311b26f4f986d24a4b7`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f8b126f56cfb316fdab75a02dbdc488ff15690439dee31a49c6485cae86a8d`  
		Last Modified: Fri, 19 Jan 2024 04:24:53 GMT  
		Size: 57.6 MB (57586943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c1d8d06015bc4ec98e98fe5803520279b807a91b9847e4780bb0adff1b3746`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e3c866daa9dfb801fec62fa08488079c59321ea36fab7b120e8f02599a3d3c`  
		Last Modified: Fri, 19 Jan 2024 04:24:54 GMT  
		Size: 65.6 MB (65587915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3376a0ffe43b2fdfc0816d7327d6544d7f6263cb27a6d8a6466a908fe8eba10`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3493b22e2fd94b3a4ed259d3dd726a60b259b9a6067cc2ad27680fd4697f01`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:0c8133bd5b9a43a416ab6809e959165556abd31a4dbf7f9b33bc84a6df72a8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12160665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3064fe20a1d0c80ee2c5f6a6def84dd702ce018e4949838dfe0c5fd2da1a14fe`

```dockerfile
```

-	Layers:
	-	`sha256:697a100cbfed71c0bb43e18be9dbbbff5a24d9b6cb8a2ac6e364b50bab70af0b`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 12.1 MB (12125923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5931c8cd77e08f878390bb365588dc7c4a80febfb2367415415f8e5a1f107da5`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-bullseye`

```console
$ docker pull mysql@sha256:26340f6de6eef7560ff5be717a044d818906e236a99ac344603785f70b5d6269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-bullseye` - linux; amd64

```console
$ docker pull mysql@sha256:c8ee75a32bfb7395c1c897d3c1889dfc2c974e99052cf68cc3c44577d4bc408e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179126921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fc62e0fca157ac0dc166c14e99d1fde95378349f1ed8e63e112a6b35a10bcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1debian11
# Thu, 18 Jan 2024 17:37:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0194d1cb63034c9bdbaa3df0c1b9d193d5ccb66b1d9b216ab46c95127647749`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ade69351f1fafe41a5ea5dbe4ec23cb4e702bb74f6f0d73d6cc12447972e79`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 4.2 MB (4207452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ef08ebf2f75e85ee5250536ee79f02c17debc80b8845d83e4fc51e920473d`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 1.5 MB (1472443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cceae24050afc033cd7605b596b43072b045b77b94f06fce705296f4b20515`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3d460e6d3f8ed993823b7bc469bd4744f56dff99df1692851d15280a1e0eb0`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 12.5 MB (12454332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113c34d227c93c29f8daa413dd4e7c88a3066d54cfb4719cc7632be952ce0b5b`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ae7eb47461cebdad48ee59bc5e8a7dada3ff578f74417fcacd741df1816c0`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816086d31d6994c1a497efd3c0b7d288de26e365e0a92c53c793966fb42ef32d`  
		Last Modified: Thu, 18 Jan 2024 23:59:16 GMT  
		Size: 129.6 MB (129564091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c63cd51ae7c7f0e9d881fc970c5b8e121606d071ee4b3f20a19ef6f1c6d3aa`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d525e1cf6fab1a8683933c035c7172fee8d20b0215455929bd23243a13e83cb0`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a763557c508841e97a158f398926568c286541275d5cccde1857899bf1e363c4`  
		Last Modified: Thu, 18 Jan 2024 23:59:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-bullseye` - unknown; unknown

```console
$ docker pull mysql@sha256:2b88e2680c65055450d6a57cfa3ea40c0ccbc1f87a7be560a2b75c136de0e025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c6e5ad027e3627f0762bee0a62848185d4cc4d250e2de4ff78721141640b26`

```dockerfile
```

-	Layers:
	-	`sha256:326d5dfb36e31ea7aa4e0572384ba5348968e4b223581fe9cb25cc8d8e9bf463`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d99e06c03dbe372a3e70c4ce5aab293a18fd0229d5058f8561283c4e9f14895`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-debian`

```console
$ docker pull mysql@sha256:26340f6de6eef7560ff5be717a044d818906e236a99ac344603785f70b5d6269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c8ee75a32bfb7395c1c897d3c1889dfc2c974e99052cf68cc3c44577d4bc408e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179126921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fc62e0fca157ac0dc166c14e99d1fde95378349f1ed8e63e112a6b35a10bcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1debian11
# Thu, 18 Jan 2024 17:37:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0194d1cb63034c9bdbaa3df0c1b9d193d5ccb66b1d9b216ab46c95127647749`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ade69351f1fafe41a5ea5dbe4ec23cb4e702bb74f6f0d73d6cc12447972e79`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 4.2 MB (4207452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ef08ebf2f75e85ee5250536ee79f02c17debc80b8845d83e4fc51e920473d`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 1.5 MB (1472443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cceae24050afc033cd7605b596b43072b045b77b94f06fce705296f4b20515`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3d460e6d3f8ed993823b7bc469bd4744f56dff99df1692851d15280a1e0eb0`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 12.5 MB (12454332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113c34d227c93c29f8daa413dd4e7c88a3066d54cfb4719cc7632be952ce0b5b`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7ae7eb47461cebdad48ee59bc5e8a7dada3ff578f74417fcacd741df1816c0`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816086d31d6994c1a497efd3c0b7d288de26e365e0a92c53c793966fb42ef32d`  
		Last Modified: Thu, 18 Jan 2024 23:59:16 GMT  
		Size: 129.6 MB (129564091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c63cd51ae7c7f0e9d881fc970c5b8e121606d071ee4b3f20a19ef6f1c6d3aa`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d525e1cf6fab1a8683933c035c7172fee8d20b0215455929bd23243a13e83cb0`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a763557c508841e97a158f398926568c286541275d5cccde1857899bf1e363c4`  
		Last Modified: Thu, 18 Jan 2024 23:59:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:2b88e2680c65055450d6a57cfa3ea40c0ccbc1f87a7be560a2b75c136de0e025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c6e5ad027e3627f0762bee0a62848185d4cc4d250e2de4ff78721141640b26`

```dockerfile
```

-	Layers:
	-	`sha256:326d5dfb36e31ea7aa4e0572384ba5348968e4b223581fe9cb25cc8d8e9bf463`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 3.6 MB (3552993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d99e06c03dbe372a3e70c4ce5aab293a18fd0229d5058f8561283c4e9f14895`  
		Last Modified: Thu, 18 Jan 2024 23:59:12 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oracle`

```console
$ docker pull mysql@sha256:3f75dccd64fffa40a06a4a9256206280a5ddc3e26dea3f1ab0df35b2cc12f472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:094a1638b290a1c5d5faa3f06ac2e3ed975947594db4a60aadc58a92e3d0820b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174711701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6188b3dc37c427f01aac2e8fc2b153044f2861becb8fd0f402bcabb429d71c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e714ea5470c150d90ee69da1f028674313e515f5b3c54fe94e3896b3aa5524`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ada0981f60fda3708effe5ca1e896bd17b0e307b951d76696b8d6cad59466`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae11d1b9d69faaee9664ecf939a2c7fc88ed73d135269e353163b39934f4876`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 4.6 MB (4590811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9be74ddc84185eafd024e29063043eee015ec174ac612c1250d3d7ebe47b44`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a59c7182522928e2dc091099a5f00ac4d95cbfa080182995eb8175bc35854d`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42afee6c9cb6ee9efac8fb6bf9505d3d3c42fd6ea8ef12007237f7946777b9`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 58.5 MB (58506468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1f586b2e2abf128a177a2e00b54fecbaca5eb23a9c6b6e8a29bffb6527f6a`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210e58b61fa3726a89826dcbcd43a93e07c6ae9b8257082c1d15e89b878b05fd`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 59.3 MB (59300444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9719ad703de58410c05950e5f3b8d291ab3dce45ab456dcf1fbe3e1f232105f`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef92b20c8ec10ade9d1228ef999a5ff3afd443bea12717145c725d96c41e6d1`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8540b9c4cc8b6176af7013e47d420475cbb11377db6f209ebb8f4fd6f7b8e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7b68aa9d27289d647980a35d50f6b331fddb6e074ad05d65c348d076bbf97a`

```dockerfile
```

-	Layers:
	-	`sha256:864b84a5a9c97ee3b88f35bfa7242eecb3f4e13fa57d186c6f4006e317b546e4`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 12.1 MB (12127343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4792e46ce9509aea17bf39c44c30177fc1bc7feb00be1c267c9728b2ae929faf`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c6a27a7f19e497f3ae4c305466d97c7addcad4e4e13ff5a37e4ef27fa4f5eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178480867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e203202cb04420ea6d2723bc9bcab569484343079a91b9d57e996b3d2ae2305`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ca054b36e90122d41f319ab5b71780b711822ba16af311b26f4f986d24a4b7`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f8b126f56cfb316fdab75a02dbdc488ff15690439dee31a49c6485cae86a8d`  
		Last Modified: Fri, 19 Jan 2024 04:24:53 GMT  
		Size: 57.6 MB (57586943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c1d8d06015bc4ec98e98fe5803520279b807a91b9847e4780bb0adff1b3746`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e3c866daa9dfb801fec62fa08488079c59321ea36fab7b120e8f02599a3d3c`  
		Last Modified: Fri, 19 Jan 2024 04:24:54 GMT  
		Size: 65.6 MB (65587915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3376a0ffe43b2fdfc0816d7327d6544d7f6263cb27a6d8a6466a908fe8eba10`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3493b22e2fd94b3a4ed259d3dd726a60b259b9a6067cc2ad27680fd4697f01`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0c8133bd5b9a43a416ab6809e959165556abd31a4dbf7f9b33bc84a6df72a8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12160665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3064fe20a1d0c80ee2c5f6a6def84dd702ce018e4949838dfe0c5fd2da1a14fe`

```dockerfile
```

-	Layers:
	-	`sha256:697a100cbfed71c0bb43e18be9dbbbff5a24d9b6cb8a2ac6e364b50bab70af0b`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 12.1 MB (12125923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5931c8cd77e08f878390bb365588dc7c4a80febfb2367415415f8e5a1f107da5`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oraclelinux8`

```console
$ docker pull mysql@sha256:3f75dccd64fffa40a06a4a9256206280a5ddc3e26dea3f1ab0df35b2cc12f472
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:094a1638b290a1c5d5faa3f06ac2e3ed975947594db4a60aadc58a92e3d0820b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174711701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6188b3dc37c427f01aac2e8fc2b153044f2861becb8fd0f402bcabb429d71c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e714ea5470c150d90ee69da1f028674313e515f5b3c54fe94e3896b3aa5524`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ada0981f60fda3708effe5ca1e896bd17b0e307b951d76696b8d6cad59466`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 982.8 KB (982809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae11d1b9d69faaee9664ecf939a2c7fc88ed73d135269e353163b39934f4876`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 4.6 MB (4590811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9be74ddc84185eafd024e29063043eee015ec174ac612c1250d3d7ebe47b44`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a59c7182522928e2dc091099a5f00ac4d95cbfa080182995eb8175bc35854d`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42afee6c9cb6ee9efac8fb6bf9505d3d3c42fd6ea8ef12007237f7946777b9`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 58.5 MB (58506468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1f586b2e2abf128a177a2e00b54fecbaca5eb23a9c6b6e8a29bffb6527f6a`  
		Last Modified: Fri, 19 Jan 2024 00:00:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210e58b61fa3726a89826dcbcd43a93e07c6ae9b8257082c1d15e89b878b05fd`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 59.3 MB (59300444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9719ad703de58410c05950e5f3b8d291ab3dce45ab456dcf1fbe3e1f232105f`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef92b20c8ec10ade9d1228ef999a5ff3afd443bea12717145c725d96c41e6d1`  
		Last Modified: Fri, 19 Jan 2024 00:00:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:8540b9c4cc8b6176af7013e47d420475cbb11377db6f209ebb8f4fd6f7b8e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7b68aa9d27289d647980a35d50f6b331fddb6e074ad05d65c348d076bbf97a`

```dockerfile
```

-	Layers:
	-	`sha256:864b84a5a9c97ee3b88f35bfa7242eecb3f4e13fa57d186c6f4006e317b546e4`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 12.1 MB (12127343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4792e46ce9509aea17bf39c44c30177fc1bc7feb00be1c267c9728b2ae929faf`  
		Last Modified: Fri, 19 Jan 2024 00:00:17 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2c6a27a7f19e497f3ae4c305466d97c7addcad4e4e13ff5a37e4ef27fa4f5eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178480867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e203202cb04420ea6d2723bc9bcab569484343079a91b9d57e996b3d2ae2305`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ca054b36e90122d41f319ab5b71780b711822ba16af311b26f4f986d24a4b7`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f8b126f56cfb316fdab75a02dbdc488ff15690439dee31a49c6485cae86a8d`  
		Last Modified: Fri, 19 Jan 2024 04:24:53 GMT  
		Size: 57.6 MB (57586943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c1d8d06015bc4ec98e98fe5803520279b807a91b9847e4780bb0adff1b3746`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e3c866daa9dfb801fec62fa08488079c59321ea36fab7b120e8f02599a3d3c`  
		Last Modified: Fri, 19 Jan 2024 04:24:54 GMT  
		Size: 65.6 MB (65587915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3376a0ffe43b2fdfc0816d7327d6544d7f6263cb27a6d8a6466a908fe8eba10`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 5.2 KB (5179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3493b22e2fd94b3a4ed259d3dd726a60b259b9a6067cc2ad27680fd4697f01`  
		Last Modified: Fri, 19 Jan 2024 04:24:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:0c8133bd5b9a43a416ab6809e959165556abd31a4dbf7f9b33bc84a6df72a8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12160665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3064fe20a1d0c80ee2c5f6a6def84dd702ce018e4949838dfe0c5fd2da1a14fe`

```dockerfile
```

-	Layers:
	-	`sha256:697a100cbfed71c0bb43e18be9dbbbff5a24d9b6cb8a2ac6e364b50bab70af0b`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 12.1 MB (12125923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5931c8cd77e08f878390bb365588dc7c4a80febfb2367415415f8e5a1f107da5`  
		Last Modified: Fri, 19 Jan 2024 04:24:51 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oracle`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oraclelinux8`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oracle`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oraclelinux8`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux8`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux8`

```console
$ docker pull mysql@sha256:d7c20c5ba268c558f4fac62977f8c7125bde0630ff8946b08dde44135ef40df3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:6d5a11994be8ca5e4cfaf4d370219f6eb6ef8fb41d57f9ed1568a93ffd5471ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183362882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b21e040954f63d922725c2d049cf2a0dfbad5522e8d3e14c36f1823ab3f5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a921059e3898005818f7f80347bafc9800da5d427517f0713d2db0d167a0`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85878fb9bb201455b25020f87c8a00ecd14a7ff7e95f5eac360609b47c40e34`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 982.8 KB (982811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16f3fd26a8227c3566f7b9f27ec3ad511b3f28551ea9bc1a2decd885136709f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 4.6 MB (4590753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd51b5329cbeda564171e38873f6afa0ed11eecc5be923170862f1be7dcff0f`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374d2f7f3267229ec55c2bd4fc4ce43ab0e34aeb60c297c7e83da433cc260cc0`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1bb2c95740adb15e9e07fe75f7788e4f767c4048041b448b55fedd60d05cf`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.1 MB (63086154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905405360553567280bcac35bbf3b613048ee32a9e8c43ef1f3690c8609de7`  
		Last Modified: Fri, 19 Jan 2024 00:00:14 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd2da03be475c108253eb3d1f98e7567fde5455fe95af2d645cb2cfb99949`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 63.4 MB (63372101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1aa788d17b88e63b294e49ca7166003652f4df88db20739aa2a4847d32f9f`  
		Last Modified: Fri, 19 Jan 2024 00:00:15 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d5e3a0efc9f1128ba5339dab74a16a3007b18a313556bd8e84274b3eb535964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72ddd7e2fc867360cb0fc75731100509343832040c1772c6e9ea0c37b22f53`

```dockerfile
```

-	Layers:
	-	`sha256:f7a868c5536bc5b2a94aaad3135e4987c970721c5b00d2c683ab274e1c2c2c44`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 12.1 MB (12130335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1818f978b3af2b1b5f94ac03b4b6ea40fb7368e22dc876cc3d201c8031983ae3`  
		Last Modified: Fri, 19 Jan 2024 00:00:13 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8139ad4615f5cc4429677c883b192a9d48dd7a91a8df591d5c28b25101ba3731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181367614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b068ea59c6773ae58f27b4f289fecbb12cc416ba2d839736f8c62ad93d43fd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2cec5cf6db11b1ccfb2eece22d4b387b62f30a7e328795522e23241b915c40`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703d567fd0e9d63ed6a6cdc8d7c80d20a42c77fec1490c66b149c1465d70734`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 913.0 KB (912961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5675f5f5a69907e9069105931e0953815be44e5e525f414bf5f610186ae076`  
		Last Modified: Thu, 18 Jan 2024 10:39:19 GMT  
		Size: 4.3 MB (4309027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28476d81f3224aeda05a68f40337178b76109129d56f12383f9ed1305a33593e`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccea770348da3d43e10972c7556c26b99b432d847d4acbee6bf07f1576174ab5`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d004c68312b5980a24489336fbc4179ab5d58734e4da44f2ec52cbed62cb3`  
		Last Modified: Fri, 19 Jan 2024 04:23:04 GMT  
		Size: 62.0 MB (62044786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f7eaf293208f8279f94d564450d6de51401e39a35381cc514986811fa88bff`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03498da0acb42543d331a555610abe3498636b5582dc5e7bf1144d97bc1b6a5a`  
		Last Modified: Fri, 19 Jan 2024 04:23:05 GMT  
		Size: 64.0 MB (64016926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00456c5c10e446064a6cc916dd40993711017e1b276f4949c26e8f159323b2c0`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:58831b3afdc8a5345619e611bba97388d3c4935b8560e2c93551317b0778dd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aead19231860760ce33aa63604f4e08f336b0bdb4a9cc581d6f4b375c54d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e95f01684b49946a05ace4be71f77286af037390dd952d7dfd05d3e3ad455bb`  
		Last Modified: Fri, 19 Jan 2024 04:23:03 GMT  
		Size: 12.1 MB (12128933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f029ed48148b5b44a5a7318644ea8eca35e514c60c3780cffd012ee37ad9571`  
		Last Modified: Fri, 19 Jan 2024 04:23:02 GMT  
		Size: 35.1 KB (35119 bytes)  
		MIME: application/vnd.in-toto+json
