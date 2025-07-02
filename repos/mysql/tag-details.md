<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux9`](#mysql8-oraclelinux9)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bookworm`](#mysql80-bookworm)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux9`](#mysql80-oraclelinux9)
-	[`mysql:8.0.42`](#mysql8042)
-	[`mysql:8.0.42-bookworm`](#mysql8042-bookworm)
-	[`mysql:8.0.42-debian`](#mysql8042-debian)
-	[`mysql:8.0.42-oracle`](#mysql8042-oracle)
-	[`mysql:8.0.42-oraclelinux9`](#mysql8042-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.5`](#mysql845)
-	[`mysql:8.4.5-oracle`](#mysql845-oracle)
-	[`mysql:8.4.5-oraclelinux9`](#mysql845-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.3`](#mysql93)
-	[`mysql:9.3-oracle`](#mysql93-oracle)
-	[`mysql:9.3-oraclelinux9`](#mysql93-oraclelinux9)
-	[`mysql:9.3.0`](#mysql930)
-	[`mysql:9.3.0-oracle`](#mysql930-oracle)
-	[`mysql:9.3.0-oraclelinux9`](#mysql930-oraclelinux9)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux9`](#mysqlinnovation-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:4445b2668d41143cb50e471ee207f8822006249b6859b24f7e12479684def5d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:4a31a2a4e6d37d63bfcdf57b0e26a695091042dca900ffedf697bc6119804545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235100849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84914bb1b3652da2058c47e6444ded39d7ebb6260aa4e4ad22a4804d71179a9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d9502df6c787e6e54f87ec92b80c60899bf7505306f9b55ad272b90d4f06b`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79935e3fc39af3c8bf3efa9fcf15d9e61abe2272518913d7fd7770a5c0321568`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8080464255333543e2119a2d0500c671825499ccabc57c5831faa5f2c005f6f7`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 6.8 MB (6814116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8070e4772c55f8e7e5b90f6729a328b2a665f7c3d620d7bd1864680e4fa2428`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8496612335ab65259a844cfb1b8560786a4c6156a2379394afa537ae1f6a93f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36001d754a063c9d74a97d99da1cddfc2c0aeb7e27b901b060f7850d6f866a10`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 49.7 MB (49674842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a94b59cf5d807c390347e0b1da39a8c9873bd8237d3df5ad7a14f862c3a880f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d26a4e5137d1c838ebdf1ab359395e73cedf49a01ce45498c80437740b86d81`  
		Last Modified: Wed, 02 Jul 2025 00:00:57 GMT  
		Size: 128.1 MB (128118747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7cef7deccaf087f3c5969bc195900516819586da3c9d55fc4f37f7212050a`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d8b94336b4a67e7f5a46ac75fa206830c27f57c0cb9ceecd7d29eec28adb`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:50b8505819cc322335a85df45ae518ce45d5004ba0f8dd24e5099e078b3af5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbdaed4fd7d7691890f3da76e88d9a2027aa24d2c106f32a8e5a586277a6919`

```dockerfile
```

-	Layers:
	-	`sha256:8f01991251dfaa09688856c42d030a53fab51b427db1b5220a04c620eb162881`  
		Last Modified: Wed, 02 Jul 2025 00:02:26 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64512f1e20f625e6cb3d609690c8154dfea9b3fb6901fee58f7d6857c42d4207`  
		Last Modified: Wed, 02 Jul 2025 00:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45e77ec8aa0d8abace4c1ee11130438e8db601bb447e4dc3279f35f892e0243a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230646741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e66132121e28dff4f4d83d13360978428b9e61f7dd446a81438721f1878b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86fc3e3ddf962ce91620ea6567ebdb5b0fd36492812db8387ae7ade389f5a3`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289837eaafb3bb3c92417a432fb4b7323eaafee1c91e1cd66d5edeafc7ccd849`  
		Last Modified: Wed, 02 Jul 2025 05:59:08 GMT  
		Size: 48.5 MB (48537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cfbf919cfc244e20abf47a102dfd135bf36fbcce57bec601241ee9e5b8add9`  
		Last Modified: Wed, 02 Jul 2025 05:58:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23caa426cd24a0cac467a4b7b9cd8fa8cfc4b758f1335e0aaacdb0d278b83c`  
		Last Modified: Wed, 02 Jul 2025 05:59:07 GMT  
		Size: 126.7 MB (126652935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb896b3d40dcb6e9de2eb9924478d15737eeceb85e2218e15ba94b10238de`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28674eb9f8fc6c87d3dd37e81022d66327a4cacd7709b8338ab0873ecae967e7`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2803952c05f12cd48bf56ed1e281fc36be35be0d41759a0c90a262831d119ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cd9878b67dacc9f9fb008ab00bf90c9e833009cc05fd2d5cdf8676066134b3`

```dockerfile
```

-	Layers:
	-	`sha256:5e62ede72ec99f52c832b3af51a3ee02b3007898b90b227795aa40250c0defb4`  
		Last Modified: Wed, 02 Jul 2025 09:02:29 GMT  
		Size: 14.0 MB (14031628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8ccdb20060883a4a99d0250c82aec298db351e2e1c9514ea2f6fc24f3d5bf1`  
		Last Modified: Wed, 02 Jul 2025 09:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:2483bcb1c68f60d85429dfe66fc236a35f19a84a3aae7a35bdc1d872d37b58c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:672f0301facb993cdecc1d3d949479f2a5c11ac0ab21c0635434916b562c6eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183344316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5268a725ec36b74de16a6d0983eff56f9c6d056682e7d25f9261c5f62e68880f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e300dd893808c8e4e04714e9ef92e6b12b8f0601662b538debbde601b6333b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8db1fb705b272a801ffb0bd78719197385400f2c95be9113d127e9865a730`  
		Last Modified: Tue, 01 Jul 2025 02:27:54 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e442632c9cd8d93461339ae6ecb4580d9baebea2bc3951306cf419c6c73ca6b0`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 1.4 MB (1446058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e78685c7a891085c9549dd35b2a7ffd0ea5e5db94b3c81dd6d3951d547f1255`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0d9806e336e6ab0a88851724773900bcfb2a039cc36fa2a22369f3ec08c3fc`  
		Last Modified: Tue, 01 Jul 2025 02:27:54 GMT  
		Size: 15.3 MB (15295862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2f49bfb7f72978758596624c72f08744a3d22643d00594e62385905562317`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a54caa06c1e1b9b470392302f5dabf8a88f8a9560cabe8463a1642813359f`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd65240f266da3864ad3ca8ee08236ec8f4454e543c4cce9b1e90f8d1c3b94dd`  
		Last Modified: Tue, 01 Jul 2025 06:02:47 GMT  
		Size: 133.9 MB (133939199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1863c0633b341908167fee1e35056e1968ce60aae33d2db432633014ae321319`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82cc144d23c60c2c46ada93d5f2c067815b8bfa81ac20ec35cb09d1d64782b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31771b7b5c87dfd75d73b84907d3aa621bd72ed7f6c2ee8eaad25f001ab97b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:3e5cd7df22c8ec140c8154aed2e54cccf1e211596465f1846b17327f24597b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb8e204770b3cf97a82fbbc6d6c579288ecd3b25c6f549520a82f7b1af2e813`

```dockerfile
```

-	Layers:
	-	`sha256:baf76121c1a9cf9a61e59e841618059873e3e4257778900fa27b8a09d83e24b3`  
		Last Modified: Tue, 01 Jul 2025 06:02:22 GMT  
		Size: 4.2 MB (4162010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f85e195fa8c6e128a3106d0214ff4205ce49618491a76baa7eb4be221d5139e`  
		Last Modified: Tue, 01 Jul 2025 06:02:23 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:2483bcb1c68f60d85429dfe66fc236a35f19a84a3aae7a35bdc1d872d37b58c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:672f0301facb993cdecc1d3d949479f2a5c11ac0ab21c0635434916b562c6eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183344316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5268a725ec36b74de16a6d0983eff56f9c6d056682e7d25f9261c5f62e68880f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e300dd893808c8e4e04714e9ef92e6b12b8f0601662b538debbde601b6333b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8db1fb705b272a801ffb0bd78719197385400f2c95be9113d127e9865a730`  
		Last Modified: Tue, 01 Jul 2025 02:27:54 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e442632c9cd8d93461339ae6ecb4580d9baebea2bc3951306cf419c6c73ca6b0`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 1.4 MB (1446058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e78685c7a891085c9549dd35b2a7ffd0ea5e5db94b3c81dd6d3951d547f1255`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0d9806e336e6ab0a88851724773900bcfb2a039cc36fa2a22369f3ec08c3fc`  
		Last Modified: Tue, 01 Jul 2025 02:27:54 GMT  
		Size: 15.3 MB (15295862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2f49bfb7f72978758596624c72f08744a3d22643d00594e62385905562317`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a54caa06c1e1b9b470392302f5dabf8a88f8a9560cabe8463a1642813359f`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd65240f266da3864ad3ca8ee08236ec8f4454e543c4cce9b1e90f8d1c3b94dd`  
		Last Modified: Tue, 01 Jul 2025 06:02:47 GMT  
		Size: 133.9 MB (133939199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1863c0633b341908167fee1e35056e1968ce60aae33d2db432633014ae321319`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82cc144d23c60c2c46ada93d5f2c067815b8bfa81ac20ec35cb09d1d64782b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31771b7b5c87dfd75d73b84907d3aa621bd72ed7f6c2ee8eaad25f001ab97b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:3e5cd7df22c8ec140c8154aed2e54cccf1e211596465f1846b17327f24597b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb8e204770b3cf97a82fbbc6d6c579288ecd3b25c6f549520a82f7b1af2e813`

```dockerfile
```

-	Layers:
	-	`sha256:baf76121c1a9cf9a61e59e841618059873e3e4257778900fa27b8a09d83e24b3`  
		Last Modified: Tue, 01 Jul 2025 06:02:22 GMT  
		Size: 4.2 MB (4162010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f85e195fa8c6e128a3106d0214ff4205ce49618491a76baa7eb4be221d5139e`  
		Last Modified: Tue, 01 Jul 2025 06:02:23 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:4445b2668d41143cb50e471ee207f8822006249b6859b24f7e12479684def5d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:4a31a2a4e6d37d63bfcdf57b0e26a695091042dca900ffedf697bc6119804545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235100849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84914bb1b3652da2058c47e6444ded39d7ebb6260aa4e4ad22a4804d71179a9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d9502df6c787e6e54f87ec92b80c60899bf7505306f9b55ad272b90d4f06b`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79935e3fc39af3c8bf3efa9fcf15d9e61abe2272518913d7fd7770a5c0321568`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8080464255333543e2119a2d0500c671825499ccabc57c5831faa5f2c005f6f7`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 6.8 MB (6814116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8070e4772c55f8e7e5b90f6729a328b2a665f7c3d620d7bd1864680e4fa2428`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8496612335ab65259a844cfb1b8560786a4c6156a2379394afa537ae1f6a93f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36001d754a063c9d74a97d99da1cddfc2c0aeb7e27b901b060f7850d6f866a10`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 49.7 MB (49674842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a94b59cf5d807c390347e0b1da39a8c9873bd8237d3df5ad7a14f862c3a880f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d26a4e5137d1c838ebdf1ab359395e73cedf49a01ce45498c80437740b86d81`  
		Last Modified: Wed, 02 Jul 2025 00:00:57 GMT  
		Size: 128.1 MB (128118747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7cef7deccaf087f3c5969bc195900516819586da3c9d55fc4f37f7212050a`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d8b94336b4a67e7f5a46ac75fa206830c27f57c0cb9ceecd7d29eec28adb`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:50b8505819cc322335a85df45ae518ce45d5004ba0f8dd24e5099e078b3af5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbdaed4fd7d7691890f3da76e88d9a2027aa24d2c106f32a8e5a586277a6919`

```dockerfile
```

-	Layers:
	-	`sha256:8f01991251dfaa09688856c42d030a53fab51b427db1b5220a04c620eb162881`  
		Last Modified: Wed, 02 Jul 2025 00:02:26 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64512f1e20f625e6cb3d609690c8154dfea9b3fb6901fee58f7d6857c42d4207`  
		Last Modified: Wed, 02 Jul 2025 00:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45e77ec8aa0d8abace4c1ee11130438e8db601bb447e4dc3279f35f892e0243a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230646741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e66132121e28dff4f4d83d13360978428b9e61f7dd446a81438721f1878b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86fc3e3ddf962ce91620ea6567ebdb5b0fd36492812db8387ae7ade389f5a3`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289837eaafb3bb3c92417a432fb4b7323eaafee1c91e1cd66d5edeafc7ccd849`  
		Last Modified: Wed, 02 Jul 2025 05:59:08 GMT  
		Size: 48.5 MB (48537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cfbf919cfc244e20abf47a102dfd135bf36fbcce57bec601241ee9e5b8add9`  
		Last Modified: Wed, 02 Jul 2025 05:58:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23caa426cd24a0cac467a4b7b9cd8fa8cfc4b758f1335e0aaacdb0d278b83c`  
		Last Modified: Wed, 02 Jul 2025 05:59:07 GMT  
		Size: 126.7 MB (126652935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb896b3d40dcb6e9de2eb9924478d15737eeceb85e2218e15ba94b10238de`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28674eb9f8fc6c87d3dd37e81022d66327a4cacd7709b8338ab0873ecae967e7`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2803952c05f12cd48bf56ed1e281fc36be35be0d41759a0c90a262831d119ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cd9878b67dacc9f9fb008ab00bf90c9e833009cc05fd2d5cdf8676066134b3`

```dockerfile
```

-	Layers:
	-	`sha256:5e62ede72ec99f52c832b3af51a3ee02b3007898b90b227795aa40250c0defb4`  
		Last Modified: Wed, 02 Jul 2025 09:02:29 GMT  
		Size: 14.0 MB (14031628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8ccdb20060883a4a99d0250c82aec298db351e2e1c9514ea2f6fc24f3d5bf1`  
		Last Modified: Wed, 02 Jul 2025 09:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:4445b2668d41143cb50e471ee207f8822006249b6859b24f7e12479684def5d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:4a31a2a4e6d37d63bfcdf57b0e26a695091042dca900ffedf697bc6119804545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235100849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84914bb1b3652da2058c47e6444ded39d7ebb6260aa4e4ad22a4804d71179a9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d9502df6c787e6e54f87ec92b80c60899bf7505306f9b55ad272b90d4f06b`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79935e3fc39af3c8bf3efa9fcf15d9e61abe2272518913d7fd7770a5c0321568`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8080464255333543e2119a2d0500c671825499ccabc57c5831faa5f2c005f6f7`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 6.8 MB (6814116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8070e4772c55f8e7e5b90f6729a328b2a665f7c3d620d7bd1864680e4fa2428`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8496612335ab65259a844cfb1b8560786a4c6156a2379394afa537ae1f6a93f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36001d754a063c9d74a97d99da1cddfc2c0aeb7e27b901b060f7850d6f866a10`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 49.7 MB (49674842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a94b59cf5d807c390347e0b1da39a8c9873bd8237d3df5ad7a14f862c3a880f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d26a4e5137d1c838ebdf1ab359395e73cedf49a01ce45498c80437740b86d81`  
		Last Modified: Wed, 02 Jul 2025 00:00:57 GMT  
		Size: 128.1 MB (128118747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7cef7deccaf087f3c5969bc195900516819586da3c9d55fc4f37f7212050a`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d8b94336b4a67e7f5a46ac75fa206830c27f57c0cb9ceecd7d29eec28adb`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:50b8505819cc322335a85df45ae518ce45d5004ba0f8dd24e5099e078b3af5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbdaed4fd7d7691890f3da76e88d9a2027aa24d2c106f32a8e5a586277a6919`

```dockerfile
```

-	Layers:
	-	`sha256:8f01991251dfaa09688856c42d030a53fab51b427db1b5220a04c620eb162881`  
		Last Modified: Wed, 02 Jul 2025 00:02:26 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64512f1e20f625e6cb3d609690c8154dfea9b3fb6901fee58f7d6857c42d4207`  
		Last Modified: Wed, 02 Jul 2025 00:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45e77ec8aa0d8abace4c1ee11130438e8db601bb447e4dc3279f35f892e0243a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230646741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e66132121e28dff4f4d83d13360978428b9e61f7dd446a81438721f1878b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86fc3e3ddf962ce91620ea6567ebdb5b0fd36492812db8387ae7ade389f5a3`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289837eaafb3bb3c92417a432fb4b7323eaafee1c91e1cd66d5edeafc7ccd849`  
		Last Modified: Wed, 02 Jul 2025 05:59:08 GMT  
		Size: 48.5 MB (48537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cfbf919cfc244e20abf47a102dfd135bf36fbcce57bec601241ee9e5b8add9`  
		Last Modified: Wed, 02 Jul 2025 05:58:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23caa426cd24a0cac467a4b7b9cd8fa8cfc4b758f1335e0aaacdb0d278b83c`  
		Last Modified: Wed, 02 Jul 2025 05:59:07 GMT  
		Size: 126.7 MB (126652935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb896b3d40dcb6e9de2eb9924478d15737eeceb85e2218e15ba94b10238de`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28674eb9f8fc6c87d3dd37e81022d66327a4cacd7709b8338ab0873ecae967e7`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2803952c05f12cd48bf56ed1e281fc36be35be0d41759a0c90a262831d119ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cd9878b67dacc9f9fb008ab00bf90c9e833009cc05fd2d5cdf8676066134b3`

```dockerfile
```

-	Layers:
	-	`sha256:5e62ede72ec99f52c832b3af51a3ee02b3007898b90b227795aa40250c0defb4`  
		Last Modified: Wed, 02 Jul 2025 09:02:29 GMT  
		Size: 14.0 MB (14031628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8ccdb20060883a4a99d0250c82aec298db351e2e1c9514ea2f6fc24f3d5bf1`  
		Last Modified: Wed, 02 Jul 2025 09:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42`

```console
$ docker pull mysql@sha256:4445b2668d41143cb50e471ee207f8822006249b6859b24f7e12479684def5d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42` - linux; amd64

```console
$ docker pull mysql@sha256:4a31a2a4e6d37d63bfcdf57b0e26a695091042dca900ffedf697bc6119804545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235100849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84914bb1b3652da2058c47e6444ded39d7ebb6260aa4e4ad22a4804d71179a9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d9502df6c787e6e54f87ec92b80c60899bf7505306f9b55ad272b90d4f06b`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79935e3fc39af3c8bf3efa9fcf15d9e61abe2272518913d7fd7770a5c0321568`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8080464255333543e2119a2d0500c671825499ccabc57c5831faa5f2c005f6f7`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 6.8 MB (6814116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8070e4772c55f8e7e5b90f6729a328b2a665f7c3d620d7bd1864680e4fa2428`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8496612335ab65259a844cfb1b8560786a4c6156a2379394afa537ae1f6a93f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36001d754a063c9d74a97d99da1cddfc2c0aeb7e27b901b060f7850d6f866a10`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 49.7 MB (49674842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a94b59cf5d807c390347e0b1da39a8c9873bd8237d3df5ad7a14f862c3a880f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d26a4e5137d1c838ebdf1ab359395e73cedf49a01ce45498c80437740b86d81`  
		Last Modified: Wed, 02 Jul 2025 00:00:57 GMT  
		Size: 128.1 MB (128118747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7cef7deccaf087f3c5969bc195900516819586da3c9d55fc4f37f7212050a`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d8b94336b4a67e7f5a46ac75fa206830c27f57c0cb9ceecd7d29eec28adb`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42` - unknown; unknown

```console
$ docker pull mysql@sha256:50b8505819cc322335a85df45ae518ce45d5004ba0f8dd24e5099e078b3af5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbdaed4fd7d7691890f3da76e88d9a2027aa24d2c106f32a8e5a586277a6919`

```dockerfile
```

-	Layers:
	-	`sha256:8f01991251dfaa09688856c42d030a53fab51b427db1b5220a04c620eb162881`  
		Last Modified: Wed, 02 Jul 2025 00:02:26 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64512f1e20f625e6cb3d609690c8154dfea9b3fb6901fee58f7d6857c42d4207`  
		Last Modified: Wed, 02 Jul 2025 00:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45e77ec8aa0d8abace4c1ee11130438e8db601bb447e4dc3279f35f892e0243a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230646741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e66132121e28dff4f4d83d13360978428b9e61f7dd446a81438721f1878b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86fc3e3ddf962ce91620ea6567ebdb5b0fd36492812db8387ae7ade389f5a3`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289837eaafb3bb3c92417a432fb4b7323eaafee1c91e1cd66d5edeafc7ccd849`  
		Last Modified: Wed, 02 Jul 2025 05:59:08 GMT  
		Size: 48.5 MB (48537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cfbf919cfc244e20abf47a102dfd135bf36fbcce57bec601241ee9e5b8add9`  
		Last Modified: Wed, 02 Jul 2025 05:58:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23caa426cd24a0cac467a4b7b9cd8fa8cfc4b758f1335e0aaacdb0d278b83c`  
		Last Modified: Wed, 02 Jul 2025 05:59:07 GMT  
		Size: 126.7 MB (126652935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb896b3d40dcb6e9de2eb9924478d15737eeceb85e2218e15ba94b10238de`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28674eb9f8fc6c87d3dd37e81022d66327a4cacd7709b8338ab0873ecae967e7`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42` - unknown; unknown

```console
$ docker pull mysql@sha256:2803952c05f12cd48bf56ed1e281fc36be35be0d41759a0c90a262831d119ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cd9878b67dacc9f9fb008ab00bf90c9e833009cc05fd2d5cdf8676066134b3`

```dockerfile
```

-	Layers:
	-	`sha256:5e62ede72ec99f52c832b3af51a3ee02b3007898b90b227795aa40250c0defb4`  
		Last Modified: Wed, 02 Jul 2025 09:02:29 GMT  
		Size: 14.0 MB (14031628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8ccdb20060883a4a99d0250c82aec298db351e2e1c9514ea2f6fc24f3d5bf1`  
		Last Modified: Wed, 02 Jul 2025 09:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-bookworm`

```console
$ docker pull mysql@sha256:2483bcb1c68f60d85429dfe66fc236a35f19a84a3aae7a35bdc1d872d37b58c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.42-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:672f0301facb993cdecc1d3d949479f2a5c11ac0ab21c0635434916b562c6eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183344316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5268a725ec36b74de16a6d0983eff56f9c6d056682e7d25f9261c5f62e68880f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e300dd893808c8e4e04714e9ef92e6b12b8f0601662b538debbde601b6333b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8db1fb705b272a801ffb0bd78719197385400f2c95be9113d127e9865a730`  
		Last Modified: Tue, 01 Jul 2025 02:27:54 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e442632c9cd8d93461339ae6ecb4580d9baebea2bc3951306cf419c6c73ca6b0`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 1.4 MB (1446058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e78685c7a891085c9549dd35b2a7ffd0ea5e5db94b3c81dd6d3951d547f1255`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0d9806e336e6ab0a88851724773900bcfb2a039cc36fa2a22369f3ec08c3fc`  
		Last Modified: Tue, 01 Jul 2025 02:27:54 GMT  
		Size: 15.3 MB (15295862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2f49bfb7f72978758596624c72f08744a3d22643d00594e62385905562317`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a54caa06c1e1b9b470392302f5dabf8a88f8a9560cabe8463a1642813359f`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd65240f266da3864ad3ca8ee08236ec8f4454e543c4cce9b1e90f8d1c3b94dd`  
		Last Modified: Tue, 01 Jul 2025 06:02:47 GMT  
		Size: 133.9 MB (133939199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1863c0633b341908167fee1e35056e1968ce60aae33d2db432633014ae321319`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82cc144d23c60c2c46ada93d5f2c067815b8bfa81ac20ec35cb09d1d64782b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31771b7b5c87dfd75d73b84907d3aa621bd72ed7f6c2ee8eaad25f001ab97b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:3e5cd7df22c8ec140c8154aed2e54cccf1e211596465f1846b17327f24597b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb8e204770b3cf97a82fbbc6d6c579288ecd3b25c6f549520a82f7b1af2e813`

```dockerfile
```

-	Layers:
	-	`sha256:baf76121c1a9cf9a61e59e841618059873e3e4257778900fa27b8a09d83e24b3`  
		Last Modified: Tue, 01 Jul 2025 06:02:22 GMT  
		Size: 4.2 MB (4162010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f85e195fa8c6e128a3106d0214ff4205ce49618491a76baa7eb4be221d5139e`  
		Last Modified: Tue, 01 Jul 2025 06:02:23 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-debian`

```console
$ docker pull mysql@sha256:2483bcb1c68f60d85429dfe66fc236a35f19a84a3aae7a35bdc1d872d37b58c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.42-debian` - linux; amd64

```console
$ docker pull mysql@sha256:672f0301facb993cdecc1d3d949479f2a5c11ac0ab21c0635434916b562c6eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183344316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5268a725ec36b74de16a6d0983eff56f9c6d056682e7d25f9261c5f62e68880f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Mon, 14 Apr 2025 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1debian12
# Mon, 14 Apr 2025 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e300dd893808c8e4e04714e9ef92e6b12b8f0601662b538debbde601b6333b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8db1fb705b272a801ffb0bd78719197385400f2c95be9113d127e9865a730`  
		Last Modified: Tue, 01 Jul 2025 02:27:54 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e442632c9cd8d93461339ae6ecb4580d9baebea2bc3951306cf419c6c73ca6b0`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 1.4 MB (1446058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e78685c7a891085c9549dd35b2a7ffd0ea5e5db94b3c81dd6d3951d547f1255`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0d9806e336e6ab0a88851724773900bcfb2a039cc36fa2a22369f3ec08c3fc`  
		Last Modified: Tue, 01 Jul 2025 02:27:54 GMT  
		Size: 15.3 MB (15295862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2f49bfb7f72978758596624c72f08744a3d22643d00594e62385905562317`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a54caa06c1e1b9b470392302f5dabf8a88f8a9560cabe8463a1642813359f`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd65240f266da3864ad3ca8ee08236ec8f4454e543c4cce9b1e90f8d1c3b94dd`  
		Last Modified: Tue, 01 Jul 2025 06:02:47 GMT  
		Size: 133.9 MB (133939199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1863c0633b341908167fee1e35056e1968ce60aae33d2db432633014ae321319`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de82cc144d23c60c2c46ada93d5f2c067815b8bfa81ac20ec35cb09d1d64782b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31771b7b5c87dfd75d73b84907d3aa621bd72ed7f6c2ee8eaad25f001ab97b`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:3e5cd7df22c8ec140c8154aed2e54cccf1e211596465f1846b17327f24597b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb8e204770b3cf97a82fbbc6d6c579288ecd3b25c6f549520a82f7b1af2e813`

```dockerfile
```

-	Layers:
	-	`sha256:baf76121c1a9cf9a61e59e841618059873e3e4257778900fa27b8a09d83e24b3`  
		Last Modified: Tue, 01 Jul 2025 06:02:22 GMT  
		Size: 4.2 MB (4162010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f85e195fa8c6e128a3106d0214ff4205ce49618491a76baa7eb4be221d5139e`  
		Last Modified: Tue, 01 Jul 2025 06:02:23 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-oracle`

```console
$ docker pull mysql@sha256:4445b2668d41143cb50e471ee207f8822006249b6859b24f7e12479684def5d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:4a31a2a4e6d37d63bfcdf57b0e26a695091042dca900ffedf697bc6119804545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235100849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84914bb1b3652da2058c47e6444ded39d7ebb6260aa4e4ad22a4804d71179a9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d9502df6c787e6e54f87ec92b80c60899bf7505306f9b55ad272b90d4f06b`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79935e3fc39af3c8bf3efa9fcf15d9e61abe2272518913d7fd7770a5c0321568`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8080464255333543e2119a2d0500c671825499ccabc57c5831faa5f2c005f6f7`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 6.8 MB (6814116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8070e4772c55f8e7e5b90f6729a328b2a665f7c3d620d7bd1864680e4fa2428`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8496612335ab65259a844cfb1b8560786a4c6156a2379394afa537ae1f6a93f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36001d754a063c9d74a97d99da1cddfc2c0aeb7e27b901b060f7850d6f866a10`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 49.7 MB (49674842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a94b59cf5d807c390347e0b1da39a8c9873bd8237d3df5ad7a14f862c3a880f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d26a4e5137d1c838ebdf1ab359395e73cedf49a01ce45498c80437740b86d81`  
		Last Modified: Wed, 02 Jul 2025 00:00:57 GMT  
		Size: 128.1 MB (128118747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7cef7deccaf087f3c5969bc195900516819586da3c9d55fc4f37f7212050a`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d8b94336b4a67e7f5a46ac75fa206830c27f57c0cb9ceecd7d29eec28adb`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:50b8505819cc322335a85df45ae518ce45d5004ba0f8dd24e5099e078b3af5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbdaed4fd7d7691890f3da76e88d9a2027aa24d2c106f32a8e5a586277a6919`

```dockerfile
```

-	Layers:
	-	`sha256:8f01991251dfaa09688856c42d030a53fab51b427db1b5220a04c620eb162881`  
		Last Modified: Wed, 02 Jul 2025 00:02:26 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64512f1e20f625e6cb3d609690c8154dfea9b3fb6901fee58f7d6857c42d4207`  
		Last Modified: Wed, 02 Jul 2025 00:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45e77ec8aa0d8abace4c1ee11130438e8db601bb447e4dc3279f35f892e0243a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230646741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e66132121e28dff4f4d83d13360978428b9e61f7dd446a81438721f1878b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86fc3e3ddf962ce91620ea6567ebdb5b0fd36492812db8387ae7ade389f5a3`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289837eaafb3bb3c92417a432fb4b7323eaafee1c91e1cd66d5edeafc7ccd849`  
		Last Modified: Wed, 02 Jul 2025 05:59:08 GMT  
		Size: 48.5 MB (48537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cfbf919cfc244e20abf47a102dfd135bf36fbcce57bec601241ee9e5b8add9`  
		Last Modified: Wed, 02 Jul 2025 05:58:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23caa426cd24a0cac467a4b7b9cd8fa8cfc4b758f1335e0aaacdb0d278b83c`  
		Last Modified: Wed, 02 Jul 2025 05:59:07 GMT  
		Size: 126.7 MB (126652935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb896b3d40dcb6e9de2eb9924478d15737eeceb85e2218e15ba94b10238de`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28674eb9f8fc6c87d3dd37e81022d66327a4cacd7709b8338ab0873ecae967e7`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2803952c05f12cd48bf56ed1e281fc36be35be0d41759a0c90a262831d119ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cd9878b67dacc9f9fb008ab00bf90c9e833009cc05fd2d5cdf8676066134b3`

```dockerfile
```

-	Layers:
	-	`sha256:5e62ede72ec99f52c832b3af51a3ee02b3007898b90b227795aa40250c0defb4`  
		Last Modified: Wed, 02 Jul 2025 09:02:29 GMT  
		Size: 14.0 MB (14031628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8ccdb20060883a4a99d0250c82aec298db351e2e1c9514ea2f6fc24f3d5bf1`  
		Last Modified: Wed, 02 Jul 2025 09:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.42-oraclelinux9`

```console
$ docker pull mysql@sha256:4445b2668d41143cb50e471ee207f8822006249b6859b24f7e12479684def5d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.42-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:4a31a2a4e6d37d63bfcdf57b0e26a695091042dca900ffedf697bc6119804545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235100849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84914bb1b3652da2058c47e6444ded39d7ebb6260aa4e4ad22a4804d71179a9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d9502df6c787e6e54f87ec92b80c60899bf7505306f9b55ad272b90d4f06b`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79935e3fc39af3c8bf3efa9fcf15d9e61abe2272518913d7fd7770a5c0321568`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8080464255333543e2119a2d0500c671825499ccabc57c5831faa5f2c005f6f7`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 6.8 MB (6814116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8070e4772c55f8e7e5b90f6729a328b2a665f7c3d620d7bd1864680e4fa2428`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8496612335ab65259a844cfb1b8560786a4c6156a2379394afa537ae1f6a93f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36001d754a063c9d74a97d99da1cddfc2c0aeb7e27b901b060f7850d6f866a10`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 49.7 MB (49674842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a94b59cf5d807c390347e0b1da39a8c9873bd8237d3df5ad7a14f862c3a880f`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d26a4e5137d1c838ebdf1ab359395e73cedf49a01ce45498c80437740b86d81`  
		Last Modified: Wed, 02 Jul 2025 00:00:57 GMT  
		Size: 128.1 MB (128118747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e7cef7deccaf087f3c5969bc195900516819586da3c9d55fc4f37f7212050a`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d8b94336b4a67e7f5a46ac75fa206830c27f57c0cb9ceecd7d29eec28adb`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:50b8505819cc322335a85df45ae518ce45d5004ba0f8dd24e5099e078b3af5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbdaed4fd7d7691890f3da76e88d9a2027aa24d2c106f32a8e5a586277a6919`

```dockerfile
```

-	Layers:
	-	`sha256:8f01991251dfaa09688856c42d030a53fab51b427db1b5220a04c620eb162881`  
		Last Modified: Wed, 02 Jul 2025 00:02:26 GMT  
		Size: 14.0 MB (14033281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64512f1e20f625e6cb3d609690c8154dfea9b3fb6901fee58f7d6857c42d4207`  
		Last Modified: Wed, 02 Jul 2025 00:02:27 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.42-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:45e77ec8aa0d8abace4c1ee11130438e8db601bb447e4dc3279f35f892e0243a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230646741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e66132121e28dff4f4d83d13360978428b9e61f7dd446a81438721f1878b71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 14 Apr 2025 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Apr 2025 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86fc3e3ddf962ce91620ea6567ebdb5b0fd36492812db8387ae7ade389f5a3`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289837eaafb3bb3c92417a432fb4b7323eaafee1c91e1cd66d5edeafc7ccd849`  
		Last Modified: Wed, 02 Jul 2025 05:59:08 GMT  
		Size: 48.5 MB (48537166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cfbf919cfc244e20abf47a102dfd135bf36fbcce57bec601241ee9e5b8add9`  
		Last Modified: Wed, 02 Jul 2025 05:58:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23caa426cd24a0cac467a4b7b9cd8fa8cfc4b758f1335e0aaacdb0d278b83c`  
		Last Modified: Wed, 02 Jul 2025 05:59:07 GMT  
		Size: 126.7 MB (126652935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bb896b3d40dcb6e9de2eb9924478d15737eeceb85e2218e15ba94b10238de`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28674eb9f8fc6c87d3dd37e81022d66327a4cacd7709b8338ab0873ecae967e7`  
		Last Modified: Wed, 02 Jul 2025 05:58:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.42-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2803952c05f12cd48bf56ed1e281fc36be35be0d41759a0c90a262831d119ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14066830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cd9878b67dacc9f9fb008ab00bf90c9e833009cc05fd2d5cdf8676066134b3`

```dockerfile
```

-	Layers:
	-	`sha256:5e62ede72ec99f52c832b3af51a3ee02b3007898b90b227795aa40250c0defb4`  
		Last Modified: Wed, 02 Jul 2025 09:02:29 GMT  
		Size: 14.0 MB (14031628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8ccdb20060883a4a99d0250c82aec298db351e2e1c9514ea2f6fc24f3d5bf1`  
		Last Modified: Wed, 02 Jul 2025 09:02:30 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5-oracle`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.5-oraclelinux9`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3-oracle`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3-oraclelinux9`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0-oracle`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.3.0-oraclelinux9`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.3.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.3.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.3.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:85144db2a70009020bc161bb11c34064e80e8e951b983c5fe3905ef688b54de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a9885f5505512e670b35dca63672c93e84de5b38499ee0caa59565a05edc4e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0606523372133afb755fd35fd62f3da61416989cd3fd8b91e3699fa99badc06f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d6e7bcb7357ec8d811b19f201d037fca3b01e6d7c437cc3d6b38b601434d78`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2654d9309c589f1db8ff6fb359b170158050ba4e69ba737aa02970e48706b1`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286601e5da95ccaa8f411a90fa126b016f41ca2a030c4b03d25b6a3adbf7dde`  
		Last Modified: Tue, 01 Jul 2025 21:36:56 GMT  
		Size: 6.8 MB (6814163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a60b4812aaa7b9ef027810cc157b7199b6a6e8ee35521d7fd75a3a3236a7d`  
		Last Modified: Tue, 01 Jul 2025 21:36:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09c8dfc15270fdda5e87442564921a284204f1939efc8834849fb082f929a4`  
		Last Modified: Tue, 01 Jul 2025 21:36:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87733f88db16f19e4db1d55702ee81a1531d49716016ab5d042670ee11f16e46`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 47.6 MB (47632228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3147970c2f48cdb84aa84f82e925f4d557911ee0f922d485f392d9176382a96e`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87afefe03e0f4a2e668a019849b126b375981640cc31753227024338d7a118a`  
		Last Modified: Wed, 02 Jul 2025 00:02:24 GMT  
		Size: 131.2 MB (131153116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586cfef3557ce39950b1cc05aea933e1308bce1841d1bf82fd65a87d88506e1`  
		Last Modified: Tue, 01 Jul 2025 21:36:54 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:247631dedea3d5b82ac4f56f0eba3cb573bcd6575a9766313c4c911c8c4a2842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14344353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b90276803ceb1cb55b5bc0817cdb238d553716c2c4b95eb2d1267affa67ef8`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8891ed86cf8193071f051752de2f6bab6681fa4372b60aecef30d39c49c83`  
		Last Modified: Wed, 02 Jul 2025 00:02:20 GMT  
		Size: 14.3 MB (14310102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d4e5b8258e6ca99011b82d9f7f84df3a24de9c38cb48d3bed07a984ffa119`  
		Last Modified: Wed, 02 Jul 2025 00:02:21 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:22e6e3f78dba5bdd8c610f7e6f8be6617d501f1b794ded2501889a594cdfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231484543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a6cf130b6878e8b4ba8cbcf046057725dc36c3324b2c7502f9cb75130a92b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Apr 2025 10:15:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENV MYSQL_SHELL_VERSION=8.4.5-1.el9
# Tue, 15 Apr 2025 10:15:16 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Apr 2025 10:15:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 10:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 10:15:16 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 15 Apr 2025 10:15:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47225d0b7f9af805b3fd7113ae1fa0142439bab8cbd429796e8aa77c5263b49`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e724400209677a44e8b31959d7c9d613f4be0ef0cefe11209608931d1ead88`  
		Last Modified: Wed, 02 Jul 2025 05:57:30 GMT  
		Size: 46.5 MB (46512426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bba52feec9f17087fb80ed22b04ae3c273016cdf60229d71cad0812eb9aabc`  
		Last Modified: Wed, 02 Jul 2025 05:57:25 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38424457b9cd6c2b457229ee6b15c54628ff078691216bacdbb235810ae4d2c3`  
		Last Modified: Wed, 02 Jul 2025 06:26:08 GMT  
		Size: 129.5 MB (129515592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a119c12c632bb7de9ef16bd716b13317c41a65bf5332b480445b739dc1dd714`  
		Last Modified: Wed, 02 Jul 2025 05:57:26 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:61d8d30cc58c43b2f0133bb41eae0df746e5bc96f454a4f027b2069f3f67b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14343077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6c6f458dc67b70b3e48d6bb7a0184e4e123475443fa04bf27ce31f5770969c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbb6b6411996b122f1b32ba3b38e72e76dac8d640f163b92720f0990d21407a`  
		Last Modified: Wed, 02 Jul 2025 09:02:26 GMT  
		Size: 14.3 MB (14308521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c548412281cbb8c5a0bb93e004336d006dc1384f540805715cfa79adf556b2`  
		Last Modified: Wed, 02 Jul 2025 09:02:27 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:f1049ce35b3986b84c08184de43a0b2109ae037a4a10a23ecf373a893daeadf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2a4ae1c9e3c4077748f7f4261e3b63f9e4a7e9ff4fb23c99697ff398bc2ab1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11f923fa047b37b6b0f7382e9748e1c30d6d657a288f834e4301c293398b67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2a1d21561bb67e4667351befeba3b3184cbea9a450790151c81e6555b780b`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701765b175d158a4e0ba6873d4da1c3c1b628a3481544f5c6faeb219cfdc0`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 983.0 KB (983000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f07fe1b6edd853f5d352989b494c686246cd5c0aa560c3b02123ed78dfdc5`  
		Last Modified: Tue, 01 Jul 2025 21:36:59 GMT  
		Size: 6.8 MB (6814213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c16d564ee5b0e13639d2cfeb1ec7930825eeb73fe9f3062699b4ec5a55aa6`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7a8f5c310a1a6b6712c483ff41dba980bb831bae1d1222013f2409c1a3ffd`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6048afa684017fa1e383bce01038610f987ef8534e91e60092b2246879d1149`  
		Last Modified: Tue, 01 Jul 2025 21:37:02 GMT  
		Size: 48.4 MB (48428408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56483034e3f14179e2064ddf2535f2c38ba0c5371a79fd9ed483e0f32053f6b8`  
		Last Modified: Tue, 01 Jul 2025 21:36:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45e5094a07fed3ace605f6f026a2bbf761b10dda3b65b551d4e6df777ecf0d`  
		Last Modified: Wed, 02 Jul 2025 00:02:46 GMT  
		Size: 152.4 MB (152370547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b536f25676c206ecc4a8e1e21440a337752afd2052a9fcf3169a381d47ae587`  
		Last Modified: Tue, 01 Jul 2025 21:37:04 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5bffdb060e1d647621627986b3f9cfa03e4ddb6006033e77e01c3a75bb4db3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15111918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf603610f47b58e4f009d58b611ae7bbbf5bf5bfac7b989cc6078c4fb95751`

```dockerfile
```

-	Layers:
	-	`sha256:6a5729c0127f278246dedf35d6d8a96760dfd328f287693d9a40d0cdcff545f0`  
		Last Modified: Wed, 02 Jul 2025 00:02:43 GMT  
		Size: 15.1 MB (15076600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1ac25105294cd1ff14f2c1d0e62e27edc477cde51d3ea16622d804c564f653`  
		Last Modified: Wed, 02 Jul 2025 00:02:44 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a79faff14ca5424adc27319d5a6e6bebc37549dcf54fc6df7e8f01ab9053a31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253367687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad553ffdef6996920b0e56473f5905eebb4d78cd425c64918a8bacf99b9bf2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Apr 2025 22:25:44 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["/bin/bash"]
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENV MYSQL_SHELL_VERSION=9.3.0-1.el9
# Mon, 14 Apr 2025 22:25:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Apr 2025 22:25:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 22:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 22:25:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Apr 2025 22:25:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f88db8b403df25cfb42932dcf6a13b194914adc80b949bf339643333a61b48`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b612ff3202e2ab7a504f03b942405d8c374904e09fe7a4d1b0b22f646f23e5e1`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e786723cf248ac3764f77d850e6612d67d4ba9f6b6c9969b2feb5c01bbe3`  
		Last Modified: Wed, 02 Jul 2025 05:55:59 GMT  
		Size: 6.4 MB (6446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03dc84bb9af30f1a67412d7a4c3b78737afc99832e64f8fc26d7990db213e`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6158974cd9bed66080cb1f9ed0ed5e559599204b3daf0eddb6127f1dfd04d`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f93dc8e533c54fde67fd31d45e9dbc1164a5fab57a8d6feb512f2ca730f64`  
		Last Modified: Wed, 02 Jul 2025 05:56:02 GMT  
		Size: 47.3 MB (47273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a446129f094673f8091610bb1644a8d51d1064198d5f6d3b9d4768f2e28153`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1ecd77c3ebf04090cee600bf9b4101895fad9ed105a9b0531b23a57aa48d8`  
		Last Modified: Wed, 02 Jul 2025 06:17:05 GMT  
		Size: 150.6 MB (150637907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95331af254049363921b9e47b20a9095f5a7b23926096140b0fd3d7acab81dfe`  
		Last Modified: Wed, 02 Jul 2025 05:55:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4a359b3c8e77ec9e6492736dd1e34240f7b03c3eae7847be8e28c6bb05c2952c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9226a50fc685a550a97a14b794d65b023d5e0f19a60b79cc4cceabdb833bdd`

```dockerfile
```

-	Layers:
	-	`sha256:2f7b0e007619926019b14f7b28711696c84b803a04130dfb3cf5be624c6eefea`  
		Last Modified: Wed, 02 Jul 2025 09:02:49 GMT  
		Size: 15.1 MB (15075055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a014b53f5339f368ad83cef720307ed9f33bd43ea4ecfef6a899a9f04733a37d`  
		Last Modified: Wed, 02 Jul 2025 09:02:50 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
