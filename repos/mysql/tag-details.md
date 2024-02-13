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
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux8`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:d848240fd25e2bc1c4f1f3a1f0a0f32582871feb0373dfb8203a52f390120e6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:785c62f5a95428152917132395141a1921c7f57d68b7c5734b6830ab095bed76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174754785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738c356409370f983e913d2b252deabe969dfa2fa666a6f0fa94ca8ea20b0224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e74d3ab32022dc1350b22bbfa6bffd287d8ec963c9eb85b08b8aed0f047b140`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb945026c45f9d5b90da08a8b339c7c05e7f75d37e544cd86b16895a32293e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f6baa2a8249cf1bfb3b2622e2d579f23ff3c36b044959a6ab4dfcf8e0ba4f`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 4.6 MB (4602985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ccb91f8f505b2f1ea204dbc1af4af848cbde51844c2ca725077d9c0e3eb95a`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cd46a2493b7f4bd2c4748f64f0fa1bdff970f3ff70fd4152c83f9a77674701`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdb378f692d343b4ac0a36c9e9254c9515fa31f843905147a32e0d84b856b`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 58.5 MB (58518982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a073ddd89256772dad2e4758a2ca15585abc4a3da17ae01cba59d703f1bdd`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafccc0d406ab73614d9aac2c4db5b725f981b824c1f399067f2f1eb0686585`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 59.3 MB (59313177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a686d0596495039f73b9bd805bcbb15aac55f92f50a58647cae07a2a6d496c3`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d292e5aace39851c6d26e1ed801e415d1a8aac2425e3d768ade2424dc136f12`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:a9282d2264323917bb975dfe39a4249130434f840fbb0124e1f139781cd05a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b63369f6eb4915fd194984c5b3fd382b7ec17df34500e1afb099d9bcbd73b9`

```dockerfile
```

-	Layers:
	-	`sha256:62cc5accec4f1577c94f7c945a8f14cd73d58cff5979513e4df81300bc3964d9`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 12.1 MB (12128064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86320672eb01f46c94abd52a980601424221270d89b8e9d5a40d3cf82288ce2`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 34.9 KB (34894 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4fad9e6ab6914ff59e274c9ee2dcdd21cce43627a87fa9ba9080f25eb501d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178456338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038074e3dc00495549f3348fa70670403f835c622f3048883741537cd80bc487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bc5fd6dca0220aa96bedd0d3eac4b1f21a314bff0eacc89a35fcc0e78ac9c`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabd0ea841669272fadb91a56e1fde03f6eaa10cd31eda58f04b8233eeab6ae`  
		Last Modified: Tue, 06 Feb 2024 23:31:01 GMT  
		Size: 57.6 MB (57579691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cac6c965cc5a69ec671d26f3b3fe99256cd9522c86bcb6a17b0d1a6040768`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b88eb4e54f758f8fa9a5fd3f34bff21d77ebeed22eb929b0276974e7a5641`  
		Last Modified: Tue, 06 Feb 2024 23:31:02 GMT  
		Size: 65.6 MB (65580442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21716a23f73ab8aa14e5cddf148ca416452064aaa61082fe3999494b85a1eb65`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e4950a2035c697acf38bda2515f46e38565f1c9017303c2949f5c4de0440f`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b8dfc584cc054732388b1b1deba347f8c06f946c18bbe5f07282bbb20808fa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2592a88306b583347ed5c6d81b6e27b85394c9bdf9bb53aa2a562a7e609890`

```dockerfile
```

-	Layers:
	-	`sha256:7af740df7f2970827c905e83579c055ffb6087531112179806889081b9e328e0`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa049cb8e022ec6b3d33869c3f51b22967dc89ed9844a914ee27022524819b1`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bullseye`

```console
$ docker pull mysql@sha256:36fa289a3093d456b6ec3cf0f64a5e010fbc0d29d77890c77a325835ad0cb3fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bullseye` - linux; amd64

```console
$ docker pull mysql@sha256:e6cb0513c62dd7a3697039b7fb81fbd42d09807e75f22d70854ae4a4ed2c63f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179120174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8c79c6da956ee87d3b27eadf59ee481c0bd164daa53ab1a68de20e73d8ca1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbb48f0c1c3f2d107cd38cadc70cc65fd99fabcf6ec5276e5fee29099c8fe7`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f2487dd7087482bbc00b4aec945f72a789eab337bbf526c2d9a25a748c763`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 4.2 MB (4207435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea27a519b8e6fc9ddcf29322672aa885d9a360caa4d68b7a136556da517e6d0`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 1.5 MB (1470916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28847b4866e601cd57a7977db351c2648c8c766ed1537f2fa4c011b09ed3eb3b`  
		Last Modified: Tue, 13 Feb 2024 01:54:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478b7e7c4580e76110715c607a09a5cee7481458c6cc6ce39bb4de9258f3b4b`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 12.5 MB (12450706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cb784b8bd32327953d4f61006fcd9d4db0d92d7c050de0ff0e63699b3d0587`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74ab38a27d1cf624284c824b0a180f82943208571c68dce6c5c24304c61dc85`  
		Last Modified: Tue, 13 Feb 2024 01:54:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389bfd8a4e71607571f0b129b7e1e7b36102476b51f8f0f81f2e13a7006e3fab`  
		Last Modified: Tue, 13 Feb 2024 01:54:14 GMT  
		Size: 129.6 MB (129558053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87993bc3ff606d1e6ea3be9a02cc1ea8dd548401d18eaeff8786aae78df9d704`  
		Last Modified: Tue, 13 Feb 2024 01:54:11 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa2ac706014be8f67fc2ede09151cb1ed9e2bebf32ef9321043cc4b2fa3152`  
		Last Modified: Tue, 13 Feb 2024 01:54:12 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb66ca57f9c721c6410ce112f3cf91305633949abb7d5aab803474ba367b5b`  
		Last Modified: Tue, 13 Feb 2024 01:54:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bullseye` - unknown; unknown

```console
$ docker pull mysql@sha256:0ac1883f5414cf14d84d011f5a392868afe2b4360a00276f869dd0980a4df61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c1fda15ae49b4862338c3b180b653bca45f31e746a38d6cf3ba24e881eeefa`

```dockerfile
```

-	Layers:
	-	`sha256:aa8fb89631e17ab257070073a5559aeba7144ca0a2334a554301d1e808991e57`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 3.6 MB (3644816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8830042a698d01fff65a11751b70152f1ab1938e991262ad75136430edef07`  
		Last Modified: Tue, 13 Feb 2024 01:54:08 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:36fa289a3093d456b6ec3cf0f64a5e010fbc0d29d77890c77a325835ad0cb3fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e6cb0513c62dd7a3697039b7fb81fbd42d09807e75f22d70854ae4a4ed2c63f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179120174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8c79c6da956ee87d3b27eadf59ee481c0bd164daa53ab1a68de20e73d8ca1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbb48f0c1c3f2d107cd38cadc70cc65fd99fabcf6ec5276e5fee29099c8fe7`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f2487dd7087482bbc00b4aec945f72a789eab337bbf526c2d9a25a748c763`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 4.2 MB (4207435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea27a519b8e6fc9ddcf29322672aa885d9a360caa4d68b7a136556da517e6d0`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 1.5 MB (1470916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28847b4866e601cd57a7977db351c2648c8c766ed1537f2fa4c011b09ed3eb3b`  
		Last Modified: Tue, 13 Feb 2024 01:54:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478b7e7c4580e76110715c607a09a5cee7481458c6cc6ce39bb4de9258f3b4b`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 12.5 MB (12450706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cb784b8bd32327953d4f61006fcd9d4db0d92d7c050de0ff0e63699b3d0587`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74ab38a27d1cf624284c824b0a180f82943208571c68dce6c5c24304c61dc85`  
		Last Modified: Tue, 13 Feb 2024 01:54:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389bfd8a4e71607571f0b129b7e1e7b36102476b51f8f0f81f2e13a7006e3fab`  
		Last Modified: Tue, 13 Feb 2024 01:54:14 GMT  
		Size: 129.6 MB (129558053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87993bc3ff606d1e6ea3be9a02cc1ea8dd548401d18eaeff8786aae78df9d704`  
		Last Modified: Tue, 13 Feb 2024 01:54:11 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa2ac706014be8f67fc2ede09151cb1ed9e2bebf32ef9321043cc4b2fa3152`  
		Last Modified: Tue, 13 Feb 2024 01:54:12 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb66ca57f9c721c6410ce112f3cf91305633949abb7d5aab803474ba367b5b`  
		Last Modified: Tue, 13 Feb 2024 01:54:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:0ac1883f5414cf14d84d011f5a392868afe2b4360a00276f869dd0980a4df61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c1fda15ae49b4862338c3b180b653bca45f31e746a38d6cf3ba24e881eeefa`

```dockerfile
```

-	Layers:
	-	`sha256:aa8fb89631e17ab257070073a5559aeba7144ca0a2334a554301d1e808991e57`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 3.6 MB (3644816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8830042a698d01fff65a11751b70152f1ab1938e991262ad75136430edef07`  
		Last Modified: Tue, 13 Feb 2024 01:54:08 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:d848240fd25e2bc1c4f1f3a1f0a0f32582871feb0373dfb8203a52f390120e6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:785c62f5a95428152917132395141a1921c7f57d68b7c5734b6830ab095bed76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174754785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738c356409370f983e913d2b252deabe969dfa2fa666a6f0fa94ca8ea20b0224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e74d3ab32022dc1350b22bbfa6bffd287d8ec963c9eb85b08b8aed0f047b140`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb945026c45f9d5b90da08a8b339c7c05e7f75d37e544cd86b16895a32293e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f6baa2a8249cf1bfb3b2622e2d579f23ff3c36b044959a6ab4dfcf8e0ba4f`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 4.6 MB (4602985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ccb91f8f505b2f1ea204dbc1af4af848cbde51844c2ca725077d9c0e3eb95a`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cd46a2493b7f4bd2c4748f64f0fa1bdff970f3ff70fd4152c83f9a77674701`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdb378f692d343b4ac0a36c9e9254c9515fa31f843905147a32e0d84b856b`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 58.5 MB (58518982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a073ddd89256772dad2e4758a2ca15585abc4a3da17ae01cba59d703f1bdd`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafccc0d406ab73614d9aac2c4db5b725f981b824c1f399067f2f1eb0686585`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 59.3 MB (59313177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a686d0596495039f73b9bd805bcbb15aac55f92f50a58647cae07a2a6d496c3`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d292e5aace39851c6d26e1ed801e415d1a8aac2425e3d768ade2424dc136f12`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a9282d2264323917bb975dfe39a4249130434f840fbb0124e1f139781cd05a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b63369f6eb4915fd194984c5b3fd382b7ec17df34500e1afb099d9bcbd73b9`

```dockerfile
```

-	Layers:
	-	`sha256:62cc5accec4f1577c94f7c945a8f14cd73d58cff5979513e4df81300bc3964d9`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 12.1 MB (12128064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86320672eb01f46c94abd52a980601424221270d89b8e9d5a40d3cf82288ce2`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 34.9 KB (34894 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4fad9e6ab6914ff59e274c9ee2dcdd21cce43627a87fa9ba9080f25eb501d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178456338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038074e3dc00495549f3348fa70670403f835c622f3048883741537cd80bc487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bc5fd6dca0220aa96bedd0d3eac4b1f21a314bff0eacc89a35fcc0e78ac9c`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabd0ea841669272fadb91a56e1fde03f6eaa10cd31eda58f04b8233eeab6ae`  
		Last Modified: Tue, 06 Feb 2024 23:31:01 GMT  
		Size: 57.6 MB (57579691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cac6c965cc5a69ec671d26f3b3fe99256cd9522c86bcb6a17b0d1a6040768`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b88eb4e54f758f8fa9a5fd3f34bff21d77ebeed22eb929b0276974e7a5641`  
		Last Modified: Tue, 06 Feb 2024 23:31:02 GMT  
		Size: 65.6 MB (65580442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21716a23f73ab8aa14e5cddf148ca416452064aaa61082fe3999494b85a1eb65`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e4950a2035c697acf38bda2515f46e38565f1c9017303c2949f5c4de0440f`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b8dfc584cc054732388b1b1deba347f8c06f946c18bbe5f07282bbb20808fa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2592a88306b583347ed5c6d81b6e27b85394c9bdf9bb53aa2a562a7e609890`

```dockerfile
```

-	Layers:
	-	`sha256:7af740df7f2970827c905e83579c055ffb6087531112179806889081b9e328e0`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa049cb8e022ec6b3d33869c3f51b22967dc89ed9844a914ee27022524819b1`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux8`

```console
$ docker pull mysql@sha256:d848240fd25e2bc1c4f1f3a1f0a0f32582871feb0373dfb8203a52f390120e6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:785c62f5a95428152917132395141a1921c7f57d68b7c5734b6830ab095bed76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174754785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738c356409370f983e913d2b252deabe969dfa2fa666a6f0fa94ca8ea20b0224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e74d3ab32022dc1350b22bbfa6bffd287d8ec963c9eb85b08b8aed0f047b140`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb945026c45f9d5b90da08a8b339c7c05e7f75d37e544cd86b16895a32293e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f6baa2a8249cf1bfb3b2622e2d579f23ff3c36b044959a6ab4dfcf8e0ba4f`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 4.6 MB (4602985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ccb91f8f505b2f1ea204dbc1af4af848cbde51844c2ca725077d9c0e3eb95a`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cd46a2493b7f4bd2c4748f64f0fa1bdff970f3ff70fd4152c83f9a77674701`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdb378f692d343b4ac0a36c9e9254c9515fa31f843905147a32e0d84b856b`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 58.5 MB (58518982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a073ddd89256772dad2e4758a2ca15585abc4a3da17ae01cba59d703f1bdd`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafccc0d406ab73614d9aac2c4db5b725f981b824c1f399067f2f1eb0686585`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 59.3 MB (59313177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a686d0596495039f73b9bd805bcbb15aac55f92f50a58647cae07a2a6d496c3`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d292e5aace39851c6d26e1ed801e415d1a8aac2425e3d768ade2424dc136f12`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:a9282d2264323917bb975dfe39a4249130434f840fbb0124e1f139781cd05a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b63369f6eb4915fd194984c5b3fd382b7ec17df34500e1afb099d9bcbd73b9`

```dockerfile
```

-	Layers:
	-	`sha256:62cc5accec4f1577c94f7c945a8f14cd73d58cff5979513e4df81300bc3964d9`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 12.1 MB (12128064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86320672eb01f46c94abd52a980601424221270d89b8e9d5a40d3cf82288ce2`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 34.9 KB (34894 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4fad9e6ab6914ff59e274c9ee2dcdd21cce43627a87fa9ba9080f25eb501d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178456338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038074e3dc00495549f3348fa70670403f835c622f3048883741537cd80bc487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bc5fd6dca0220aa96bedd0d3eac4b1f21a314bff0eacc89a35fcc0e78ac9c`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabd0ea841669272fadb91a56e1fde03f6eaa10cd31eda58f04b8233eeab6ae`  
		Last Modified: Tue, 06 Feb 2024 23:31:01 GMT  
		Size: 57.6 MB (57579691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cac6c965cc5a69ec671d26f3b3fe99256cd9522c86bcb6a17b0d1a6040768`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b88eb4e54f758f8fa9a5fd3f34bff21d77ebeed22eb929b0276974e7a5641`  
		Last Modified: Tue, 06 Feb 2024 23:31:02 GMT  
		Size: 65.6 MB (65580442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21716a23f73ab8aa14e5cddf148ca416452064aaa61082fe3999494b85a1eb65`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e4950a2035c697acf38bda2515f46e38565f1c9017303c2949f5c4de0440f`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:b8dfc584cc054732388b1b1deba347f8c06f946c18bbe5f07282bbb20808fa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2592a88306b583347ed5c6d81b6e27b85394c9bdf9bb53aa2a562a7e609890`

```dockerfile
```

-	Layers:
	-	`sha256:7af740df7f2970827c905e83579c055ffb6087531112179806889081b9e328e0`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa049cb8e022ec6b3d33869c3f51b22967dc89ed9844a914ee27022524819b1`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36`

```console
$ docker pull mysql@sha256:d848240fd25e2bc1c4f1f3a1f0a0f32582871feb0373dfb8203a52f390120e6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36` - linux; amd64

```console
$ docker pull mysql@sha256:785c62f5a95428152917132395141a1921c7f57d68b7c5734b6830ab095bed76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174754785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738c356409370f983e913d2b252deabe969dfa2fa666a6f0fa94ca8ea20b0224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e74d3ab32022dc1350b22bbfa6bffd287d8ec963c9eb85b08b8aed0f047b140`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb945026c45f9d5b90da08a8b339c7c05e7f75d37e544cd86b16895a32293e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f6baa2a8249cf1bfb3b2622e2d579f23ff3c36b044959a6ab4dfcf8e0ba4f`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 4.6 MB (4602985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ccb91f8f505b2f1ea204dbc1af4af848cbde51844c2ca725077d9c0e3eb95a`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cd46a2493b7f4bd2c4748f64f0fa1bdff970f3ff70fd4152c83f9a77674701`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdb378f692d343b4ac0a36c9e9254c9515fa31f843905147a32e0d84b856b`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 58.5 MB (58518982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a073ddd89256772dad2e4758a2ca15585abc4a3da17ae01cba59d703f1bdd`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafccc0d406ab73614d9aac2c4db5b725f981b824c1f399067f2f1eb0686585`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 59.3 MB (59313177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a686d0596495039f73b9bd805bcbb15aac55f92f50a58647cae07a2a6d496c3`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d292e5aace39851c6d26e1ed801e415d1a8aac2425e3d768ade2424dc136f12`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:a9282d2264323917bb975dfe39a4249130434f840fbb0124e1f139781cd05a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b63369f6eb4915fd194984c5b3fd382b7ec17df34500e1afb099d9bcbd73b9`

```dockerfile
```

-	Layers:
	-	`sha256:62cc5accec4f1577c94f7c945a8f14cd73d58cff5979513e4df81300bc3964d9`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 12.1 MB (12128064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86320672eb01f46c94abd52a980601424221270d89b8e9d5a40d3cf82288ce2`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 34.9 KB (34894 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4fad9e6ab6914ff59e274c9ee2dcdd21cce43627a87fa9ba9080f25eb501d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178456338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038074e3dc00495549f3348fa70670403f835c622f3048883741537cd80bc487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bc5fd6dca0220aa96bedd0d3eac4b1f21a314bff0eacc89a35fcc0e78ac9c`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabd0ea841669272fadb91a56e1fde03f6eaa10cd31eda58f04b8233eeab6ae`  
		Last Modified: Tue, 06 Feb 2024 23:31:01 GMT  
		Size: 57.6 MB (57579691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cac6c965cc5a69ec671d26f3b3fe99256cd9522c86bcb6a17b0d1a6040768`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b88eb4e54f758f8fa9a5fd3f34bff21d77ebeed22eb929b0276974e7a5641`  
		Last Modified: Tue, 06 Feb 2024 23:31:02 GMT  
		Size: 65.6 MB (65580442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21716a23f73ab8aa14e5cddf148ca416452064aaa61082fe3999494b85a1eb65`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e4950a2035c697acf38bda2515f46e38565f1c9017303c2949f5c4de0440f`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:b8dfc584cc054732388b1b1deba347f8c06f946c18bbe5f07282bbb20808fa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2592a88306b583347ed5c6d81b6e27b85394c9bdf9bb53aa2a562a7e609890`

```dockerfile
```

-	Layers:
	-	`sha256:7af740df7f2970827c905e83579c055ffb6087531112179806889081b9e328e0`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa049cb8e022ec6b3d33869c3f51b22967dc89ed9844a914ee27022524819b1`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-bullseye`

```console
$ docker pull mysql@sha256:36fa289a3093d456b6ec3cf0f64a5e010fbc0d29d77890c77a325835ad0cb3fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-bullseye` - linux; amd64

```console
$ docker pull mysql@sha256:e6cb0513c62dd7a3697039b7fb81fbd42d09807e75f22d70854ae4a4ed2c63f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179120174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8c79c6da956ee87d3b27eadf59ee481c0bd164daa53ab1a68de20e73d8ca1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbb48f0c1c3f2d107cd38cadc70cc65fd99fabcf6ec5276e5fee29099c8fe7`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f2487dd7087482bbc00b4aec945f72a789eab337bbf526c2d9a25a748c763`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 4.2 MB (4207435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea27a519b8e6fc9ddcf29322672aa885d9a360caa4d68b7a136556da517e6d0`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 1.5 MB (1470916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28847b4866e601cd57a7977db351c2648c8c766ed1537f2fa4c011b09ed3eb3b`  
		Last Modified: Tue, 13 Feb 2024 01:54:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478b7e7c4580e76110715c607a09a5cee7481458c6cc6ce39bb4de9258f3b4b`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 12.5 MB (12450706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cb784b8bd32327953d4f61006fcd9d4db0d92d7c050de0ff0e63699b3d0587`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74ab38a27d1cf624284c824b0a180f82943208571c68dce6c5c24304c61dc85`  
		Last Modified: Tue, 13 Feb 2024 01:54:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389bfd8a4e71607571f0b129b7e1e7b36102476b51f8f0f81f2e13a7006e3fab`  
		Last Modified: Tue, 13 Feb 2024 01:54:14 GMT  
		Size: 129.6 MB (129558053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87993bc3ff606d1e6ea3be9a02cc1ea8dd548401d18eaeff8786aae78df9d704`  
		Last Modified: Tue, 13 Feb 2024 01:54:11 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa2ac706014be8f67fc2ede09151cb1ed9e2bebf32ef9321043cc4b2fa3152`  
		Last Modified: Tue, 13 Feb 2024 01:54:12 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb66ca57f9c721c6410ce112f3cf91305633949abb7d5aab803474ba367b5b`  
		Last Modified: Tue, 13 Feb 2024 01:54:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-bullseye` - unknown; unknown

```console
$ docker pull mysql@sha256:0ac1883f5414cf14d84d011f5a392868afe2b4360a00276f869dd0980a4df61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c1fda15ae49b4862338c3b180b653bca45f31e746a38d6cf3ba24e881eeefa`

```dockerfile
```

-	Layers:
	-	`sha256:aa8fb89631e17ab257070073a5559aeba7144ca0a2334a554301d1e808991e57`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 3.6 MB (3644816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8830042a698d01fff65a11751b70152f1ab1938e991262ad75136430edef07`  
		Last Modified: Tue, 13 Feb 2024 01:54:08 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-debian`

```console
$ docker pull mysql@sha256:36fa289a3093d456b6ec3cf0f64a5e010fbc0d29d77890c77a325835ad0cb3fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e6cb0513c62dd7a3697039b7fb81fbd42d09807e75f22d70854ae4a4ed2c63f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179120174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8c79c6da956ee87d3b27eadf59ee481c0bd164daa53ab1a68de20e73d8ca1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbb48f0c1c3f2d107cd38cadc70cc65fd99fabcf6ec5276e5fee29099c8fe7`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f2487dd7087482bbc00b4aec945f72a789eab337bbf526c2d9a25a748c763`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 4.2 MB (4207435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea27a519b8e6fc9ddcf29322672aa885d9a360caa4d68b7a136556da517e6d0`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 1.5 MB (1470916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28847b4866e601cd57a7977db351c2648c8c766ed1537f2fa4c011b09ed3eb3b`  
		Last Modified: Tue, 13 Feb 2024 01:54:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478b7e7c4580e76110715c607a09a5cee7481458c6cc6ce39bb4de9258f3b4b`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 12.5 MB (12450706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cb784b8bd32327953d4f61006fcd9d4db0d92d7c050de0ff0e63699b3d0587`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74ab38a27d1cf624284c824b0a180f82943208571c68dce6c5c24304c61dc85`  
		Last Modified: Tue, 13 Feb 2024 01:54:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389bfd8a4e71607571f0b129b7e1e7b36102476b51f8f0f81f2e13a7006e3fab`  
		Last Modified: Tue, 13 Feb 2024 01:54:14 GMT  
		Size: 129.6 MB (129558053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87993bc3ff606d1e6ea3be9a02cc1ea8dd548401d18eaeff8786aae78df9d704`  
		Last Modified: Tue, 13 Feb 2024 01:54:11 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa2ac706014be8f67fc2ede09151cb1ed9e2bebf32ef9321043cc4b2fa3152`  
		Last Modified: Tue, 13 Feb 2024 01:54:12 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb66ca57f9c721c6410ce112f3cf91305633949abb7d5aab803474ba367b5b`  
		Last Modified: Tue, 13 Feb 2024 01:54:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:0ac1883f5414cf14d84d011f5a392868afe2b4360a00276f869dd0980a4df61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c1fda15ae49b4862338c3b180b653bca45f31e746a38d6cf3ba24e881eeefa`

```dockerfile
```

-	Layers:
	-	`sha256:aa8fb89631e17ab257070073a5559aeba7144ca0a2334a554301d1e808991e57`  
		Last Modified: Tue, 13 Feb 2024 01:54:09 GMT  
		Size: 3.6 MB (3644816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8830042a698d01fff65a11751b70152f1ab1938e991262ad75136430edef07`  
		Last Modified: Tue, 13 Feb 2024 01:54:08 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oracle`

```console
$ docker pull mysql@sha256:d848240fd25e2bc1c4f1f3a1f0a0f32582871feb0373dfb8203a52f390120e6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:785c62f5a95428152917132395141a1921c7f57d68b7c5734b6830ab095bed76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174754785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738c356409370f983e913d2b252deabe969dfa2fa666a6f0fa94ca8ea20b0224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e74d3ab32022dc1350b22bbfa6bffd287d8ec963c9eb85b08b8aed0f047b140`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb945026c45f9d5b90da08a8b339c7c05e7f75d37e544cd86b16895a32293e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f6baa2a8249cf1bfb3b2622e2d579f23ff3c36b044959a6ab4dfcf8e0ba4f`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 4.6 MB (4602985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ccb91f8f505b2f1ea204dbc1af4af848cbde51844c2ca725077d9c0e3eb95a`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cd46a2493b7f4bd2c4748f64f0fa1bdff970f3ff70fd4152c83f9a77674701`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdb378f692d343b4ac0a36c9e9254c9515fa31f843905147a32e0d84b856b`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 58.5 MB (58518982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a073ddd89256772dad2e4758a2ca15585abc4a3da17ae01cba59d703f1bdd`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafccc0d406ab73614d9aac2c4db5b725f981b824c1f399067f2f1eb0686585`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 59.3 MB (59313177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a686d0596495039f73b9bd805bcbb15aac55f92f50a58647cae07a2a6d496c3`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d292e5aace39851c6d26e1ed801e415d1a8aac2425e3d768ade2424dc136f12`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a9282d2264323917bb975dfe39a4249130434f840fbb0124e1f139781cd05a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b63369f6eb4915fd194984c5b3fd382b7ec17df34500e1afb099d9bcbd73b9`

```dockerfile
```

-	Layers:
	-	`sha256:62cc5accec4f1577c94f7c945a8f14cd73d58cff5979513e4df81300bc3964d9`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 12.1 MB (12128064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86320672eb01f46c94abd52a980601424221270d89b8e9d5a40d3cf82288ce2`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 34.9 KB (34894 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4fad9e6ab6914ff59e274c9ee2dcdd21cce43627a87fa9ba9080f25eb501d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178456338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038074e3dc00495549f3348fa70670403f835c622f3048883741537cd80bc487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bc5fd6dca0220aa96bedd0d3eac4b1f21a314bff0eacc89a35fcc0e78ac9c`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabd0ea841669272fadb91a56e1fde03f6eaa10cd31eda58f04b8233eeab6ae`  
		Last Modified: Tue, 06 Feb 2024 23:31:01 GMT  
		Size: 57.6 MB (57579691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cac6c965cc5a69ec671d26f3b3fe99256cd9522c86bcb6a17b0d1a6040768`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b88eb4e54f758f8fa9a5fd3f34bff21d77ebeed22eb929b0276974e7a5641`  
		Last Modified: Tue, 06 Feb 2024 23:31:02 GMT  
		Size: 65.6 MB (65580442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21716a23f73ab8aa14e5cddf148ca416452064aaa61082fe3999494b85a1eb65`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e4950a2035c697acf38bda2515f46e38565f1c9017303c2949f5c4de0440f`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b8dfc584cc054732388b1b1deba347f8c06f946c18bbe5f07282bbb20808fa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2592a88306b583347ed5c6d81b6e27b85394c9bdf9bb53aa2a562a7e609890`

```dockerfile
```

-	Layers:
	-	`sha256:7af740df7f2970827c905e83579c055ffb6087531112179806889081b9e328e0`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa049cb8e022ec6b3d33869c3f51b22967dc89ed9844a914ee27022524819b1`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oraclelinux8`

```console
$ docker pull mysql@sha256:d848240fd25e2bc1c4f1f3a1f0a0f32582871feb0373dfb8203a52f390120e6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:785c62f5a95428152917132395141a1921c7f57d68b7c5734b6830ab095bed76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174754785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738c356409370f983e913d2b252deabe969dfa2fa666a6f0fa94ca8ea20b0224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e74d3ab32022dc1350b22bbfa6bffd287d8ec963c9eb85b08b8aed0f047b140`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb945026c45f9d5b90da08a8b339c7c05e7f75d37e544cd86b16895a32293e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f6baa2a8249cf1bfb3b2622e2d579f23ff3c36b044959a6ab4dfcf8e0ba4f`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 4.6 MB (4602985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ccb91f8f505b2f1ea204dbc1af4af848cbde51844c2ca725077d9c0e3eb95a`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cd46a2493b7f4bd2c4748f64f0fa1bdff970f3ff70fd4152c83f9a77674701`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdb378f692d343b4ac0a36c9e9254c9515fa31f843905147a32e0d84b856b`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 58.5 MB (58518982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a073ddd89256772dad2e4758a2ca15585abc4a3da17ae01cba59d703f1bdd`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafccc0d406ab73614d9aac2c4db5b725f981b824c1f399067f2f1eb0686585`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 59.3 MB (59313177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a686d0596495039f73b9bd805bcbb15aac55f92f50a58647cae07a2a6d496c3`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d292e5aace39851c6d26e1ed801e415d1a8aac2425e3d768ade2424dc136f12`  
		Last Modified: Wed, 07 Feb 2024 00:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:a9282d2264323917bb975dfe39a4249130434f840fbb0124e1f139781cd05a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12162958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b63369f6eb4915fd194984c5b3fd382b7ec17df34500e1afb099d9bcbd73b9`

```dockerfile
```

-	Layers:
	-	`sha256:62cc5accec4f1577c94f7c945a8f14cd73d58cff5979513e4df81300bc3964d9`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 12.1 MB (12128064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86320672eb01f46c94abd52a980601424221270d89b8e9d5a40d3cf82288ce2`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 34.9 KB (34894 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d4fad9e6ab6914ff59e274c9ee2dcdd21cce43627a87fa9ba9080f25eb501d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178456338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038074e3dc00495549f3348fa70670403f835c622f3048883741537cd80bc487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bc5fd6dca0220aa96bedd0d3eac4b1f21a314bff0eacc89a35fcc0e78ac9c`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabd0ea841669272fadb91a56e1fde03f6eaa10cd31eda58f04b8233eeab6ae`  
		Last Modified: Tue, 06 Feb 2024 23:31:01 GMT  
		Size: 57.6 MB (57579691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cac6c965cc5a69ec671d26f3b3fe99256cd9522c86bcb6a17b0d1a6040768`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b88eb4e54f758f8fa9a5fd3f34bff21d77ebeed22eb929b0276974e7a5641`  
		Last Modified: Tue, 06 Feb 2024 23:31:02 GMT  
		Size: 65.6 MB (65580442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21716a23f73ab8aa14e5cddf148ca416452064aaa61082fe3999494b85a1eb65`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 5.2 KB (5177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e4950a2035c697acf38bda2515f46e38565f1c9017303c2949f5c4de0440f`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:b8dfc584cc054732388b1b1deba347f8c06f946c18bbe5f07282bbb20808fa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2592a88306b583347ed5c6d81b6e27b85394c9bdf9bb53aa2a562a7e609890`

```dockerfile
```

-	Layers:
	-	`sha256:7af740df7f2970827c905e83579c055ffb6087531112179806889081b9e328e0`  
		Last Modified: Tue, 06 Feb 2024 23:30:59 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa049cb8e022ec6b3d33869c3f51b22967dc89ed9844a914ee27022524819b1`  
		Last Modified: Tue, 06 Feb 2024 23:30:58 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oracle`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oraclelinux8`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oracle`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oraclelinux8`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux8`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux8`

```console
$ docker pull mysql@sha256:2a9ef1075ff30c65bbcf4f96b25a03ea3b3f492c284e6c4a612c269ce4c5bb19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:b5777db44c3714c323e47ea272a6611149ba5c9d9910235ac8056b9a4f8222a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183402774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6b635d3b6bac04e4933b9f00745dcab253da0a5a0a293c09bae043292af073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:ee9ade66919e02c9625e92c89cc2bde2568f070446ebcef5a45409031767cae2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:b8307a22608d5df5e6e46cb974e41cd9778a2521f94cbba7113f1bdcc8d10881`  
		Last Modified: Wed, 07 Feb 2024 00:04:12 GMT  
		Size: 51.3 MB (51327391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3542f2ba977b1d735d298bf323f7bc1d5bbd0cdba8aee42b3d93ce0eeebf2`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795385976c83695d78fa9a804369151ce7dd465c8faa3c028ec06d1d35aa2f47`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 982.8 KB (982805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b553142f26a7ccee8a550ad18399e7c483b1f37e7ad2614c424255ca77d136`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 4.6 MB (4603045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce6174541f907cf9d230b5d01dd524dff8a67dd70d02dd402e701b68748468`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c649012739f55b16609dce147f58e5694670df3c9ea93764badca7b73677b`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db2241c611ce88ef5e93bb0e5123016bb94269f4edb10bbf6a0569fdd3c182`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 63.1 MB (63079070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e96eb91f6b5f1ba4697138cfa901dddaa675f0f28486f7f071f741c4b28b5`  
		Last Modified: Wed, 07 Feb 2024 00:51:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b560af9a2ac6b22542aa16200ecc3f2a8f89dc436c1805bd7a87e348b6058f`  
		Last Modified: Wed, 07 Feb 2024 00:51:05 GMT  
		Size: 63.4 MB (63401128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c9925abfdf3f774ba3fb03302987e946ac26463545c7db99500d9095b6473e`  
		Last Modified: Wed, 07 Feb 2024 00:51:04 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:d548190f4246c97f5976df91e7c8cd15830e13327dc237b5d3e44537212e993a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12166310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f1bae4922c53f5a7c54569b87ee100dc4fa15221e9d390efffa012f9034975`

```dockerfile
```

-	Layers:
	-	`sha256:800ff7a43ac27f69268847501e92f3327855a0e15a83fbb5bb40b8cd50044cc8`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 12.1 MB (12131056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0e9a0ed695fed14736521d74437b514595ec602a5c15023a76c992f9d7e594`  
		Last Modified: Wed, 07 Feb 2024 00:51:02 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1fb3a55e812ef9ca0aea545719c6ade78e437ef10f5e9115f165c0cc45a1873b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181355402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f567a0830cbbe5a0f0a01155e72b194cf4e63ad5643bc15bd5493116ae9ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:cd2f7e73ea216c58af8e2422d8e7fdd8cdc79f510d74cf24416e3a3f4929f8c2 in / 
# Thu, 18 Jan 2024 17:37:32 GMT
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
	-	`sha256:0647c03756d6c2108bc331960a270dba455e910d0f076e51ad650f96b8c54db9`  
		Last Modified: Tue, 06 Feb 2024 22:06:18 GMT  
		Size: 50.1 MB (50077424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c571053c52e26a7a92e8deecce48f574cbd8ee084fe6cd2fc9364b2d1cfc83a`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6453741958d8daf97caae065cd580ced71ebaf5ef14cbe9a0ad878f0e3993f9`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e97ad7011a7fe93550602e106b83b26a19279e41a50deb11d18a3f3456df65`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 4.3 MB (4296380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f90da87686b38d8cafeb4b24913cbba39ef1087ee5a11f49df873457b8ee94`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c2a8fa113a20e70ad26c869d8c806ba8cb53e06a98021c8f5b41314706fe7`  
		Last Modified: Tue, 06 Feb 2024 23:29:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ec19ee1f6a05fc54b4114c7afb96452faab912ba78cd79801a5070cbfb097d`  
		Last Modified: Tue, 06 Feb 2024 23:29:09 GMT  
		Size: 62.0 MB (62038782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4ac7a81f6fc355b4a249c452db8f14f9b26be2a5e40f303bb76dbc9bfc7a50`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425626fff053054f82c2fdbc28682d8b6406b39b2022418edf564d7955e65cd0`  
		Last Modified: Tue, 06 Feb 2024 23:29:10 GMT  
		Size: 64.0 MB (64020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24585fbe7059bcc01d9159387cd8d647dab53bd9ba884748050d7e0754ef90c`  
		Last Modified: Tue, 06 Feb 2024 23:29:08 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:67c6025ecec8f40cae1f111867f6a508f125705d758960efdc6b66ab3e021f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffc11f2065f14f88b716ff45fb79d5273a153f5dd3274cbb5e29a2b42995ce`

```dockerfile
```

-	Layers:
	-	`sha256:ae695922a2e26a20dac635e86850bd7365283469d42f6c972805463ec4817464`  
		Last Modified: Tue, 06 Feb 2024 23:29:06 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae588ccc6f09d4905be66cbdc06c66863786ee439cb5da13bf785f866c1cd1`  
		Last Modified: Tue, 06 Feb 2024 23:29:05 GMT  
		Size: 35.3 KB (35286 bytes)  
		MIME: application/vnd.in-toto+json
