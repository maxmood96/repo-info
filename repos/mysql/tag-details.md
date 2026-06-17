<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux9`](#mysql8-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.10`](#mysql8410)
-	[`mysql:8.4.10-oracle`](#mysql8410-oracle)
-	[`mysql:8.4.10-oraclelinux9`](#mysql8410-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.7`](#mysql97)
-	[`mysql:9.7-oracle`](#mysql97-oracle)
-	[`mysql:9.7-oraclelinux9`](#mysql97-oraclelinux9)
-	[`mysql:9.7.1`](#mysql971)
-	[`mysql:9.7.1-oracle`](#mysql971-oracle)
-	[`mysql:9.7.1-oraclelinux9`](#mysql971-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:c36050afdca850f23cef85703f84c7531a5ae155a11b5ee1c60acb09937c4084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:14690274f4967ba207939c97dd79a8d6604f1d532218ea6be69c0001ddd2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238253989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1487abffa4fa011710f99e5ae2135537a5f894b7eb1380758b8915884df00e0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148eeb1a828940b6e73c890fece2c98ed8bae18635264f5a16b1353b270b5f6`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bae0286aad01d0c4e14106715011400a75f600841f3717aea2c37e462cb40c`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b1a26b51696a808ea290d78c15b586ded50d5336a9e01494a64ce4135f149b`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 6.2 MB (6170671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab549d4e00e74fbb817c909385b84887c8e3d6fc648ecdba041a510235104380`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90c44920b4ab505625930d4b6e03fdaf4f82cc28f173bfbebe273dcc3746de`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865e9f32c411ea5061231113c45a14007b4d8ba864b130d88383cf0a5231c64`  
		Last Modified: Tue, 12 May 2026 19:13:19 GMT  
		Size: 51.6 MB (51578851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b9b45fc65df7932d8232474d621e9d8ed093e481f4eecb2e9b4d94110efef`  
		Last Modified: Tue, 12 May 2026 19:13:17 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63892f528d32bf597984b4ab748e4743b95af162367aad7f59cbc0a3e0f431fc`  
		Last Modified: Tue, 12 May 2026 19:13:21 GMT  
		Size: 132.4 MB (132401957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6fc0eea0c90041e5698fa8524360c61ccfd4eca8b6c5bf7b19dda35ec150c`  
		Last Modified: Tue, 12 May 2026 19:13:18 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:ad2658b0203b3293805fa34fdfd24f6bcc5a0948e3d9bb03f01a60b42470c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46531aada87d2b105c22501c39728fa17fd6ea029ae07d0e1f4a323d62e3370e`

```dockerfile
```

-	Layers:
	-	`sha256:eb33bcfe45069ebd909020642befd333a449c8aea70239d9922fcf983e41c0be`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf9b0caf1546e3a1acae0a554491614c4a1431099e8ba1f92391c08ff6d7a3`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 33.3 KB (33298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c3d0492f593ef24dad1d77ff63bc287041d1d07de5fbc38ae095de0170421d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233039323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6a1433570c017f9e332bb3da6c5fc56eda15f9ec0090c45b85426f9c85c492`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:12:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:13:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:13:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:13:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4fc43557d62ddd16c656bf04b429b1d3d4242eefbf7376c7bc7157cb6dbc75`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e007b90980b27f2a5c2d23d2805be4fc440f42b0a234e035553f83ce3d655e3`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bd070cd646aa089f2ef70c669e9efd62ecfe9a68599d5a0f9d03cf8b691632`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 5.8 MB (5792121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864694b8117ba3d2e3c796ae5bfc310c64e3b892a30f3154f247c07046456bea`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0839df9247577841d66ffb4ab37613fd589f948d44d202ad9687bd5a871fd3a6`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7dc1e857dfa00f75aae78cb7a5429573ed43e59d2df5f037243de08b07aada`  
		Last Modified: Tue, 12 May 2026 19:13:49 GMT  
		Size: 49.8 MB (49825749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6463de6f8b7165d27c52df2c7c2b48e736918f70ef0549acf45d4dc2d00a2`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fadccec8f2daadad930e82a7556cd1aa0c890fa5a5badf033a646af1e84963`  
		Last Modified: Tue, 12 May 2026 19:13:56 GMT  
		Size: 130.8 MB (130775477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2193cf3f7597227ae8ea8c800711e55fad5964a1b3d5842223de41786572914`  
		Last Modified: Tue, 12 May 2026 19:13:48 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:96d3713d71ba400559341758e67f9aaf6de60b4ad080c1ee2839f6a95f3ac13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19386f1b3cbf6dffacb1557db1e5e8034a0cc77a5ccfe062ee5830141121d60f`

```dockerfile
```

-	Layers:
	-	`sha256:b0a38a345e943e2ce8d6374bd4b28d6a22dc7df32e8a3a18bff449dfa10ce12a`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5915ffd95d6625c09bb4c7754a4280a85a3b569a6e5f763c2024fea2602498aa`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:c36050afdca850f23cef85703f84c7531a5ae155a11b5ee1c60acb09937c4084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:14690274f4967ba207939c97dd79a8d6604f1d532218ea6be69c0001ddd2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238253989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1487abffa4fa011710f99e5ae2135537a5f894b7eb1380758b8915884df00e0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148eeb1a828940b6e73c890fece2c98ed8bae18635264f5a16b1353b270b5f6`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bae0286aad01d0c4e14106715011400a75f600841f3717aea2c37e462cb40c`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b1a26b51696a808ea290d78c15b586ded50d5336a9e01494a64ce4135f149b`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 6.2 MB (6170671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab549d4e00e74fbb817c909385b84887c8e3d6fc648ecdba041a510235104380`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90c44920b4ab505625930d4b6e03fdaf4f82cc28f173bfbebe273dcc3746de`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865e9f32c411ea5061231113c45a14007b4d8ba864b130d88383cf0a5231c64`  
		Last Modified: Tue, 12 May 2026 19:13:19 GMT  
		Size: 51.6 MB (51578851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b9b45fc65df7932d8232474d621e9d8ed093e481f4eecb2e9b4d94110efef`  
		Last Modified: Tue, 12 May 2026 19:13:17 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63892f528d32bf597984b4ab748e4743b95af162367aad7f59cbc0a3e0f431fc`  
		Last Modified: Tue, 12 May 2026 19:13:21 GMT  
		Size: 132.4 MB (132401957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6fc0eea0c90041e5698fa8524360c61ccfd4eca8b6c5bf7b19dda35ec150c`  
		Last Modified: Tue, 12 May 2026 19:13:18 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad2658b0203b3293805fa34fdfd24f6bcc5a0948e3d9bb03f01a60b42470c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46531aada87d2b105c22501c39728fa17fd6ea029ae07d0e1f4a323d62e3370e`

```dockerfile
```

-	Layers:
	-	`sha256:eb33bcfe45069ebd909020642befd333a449c8aea70239d9922fcf983e41c0be`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf9b0caf1546e3a1acae0a554491614c4a1431099e8ba1f92391c08ff6d7a3`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 33.3 KB (33298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c3d0492f593ef24dad1d77ff63bc287041d1d07de5fbc38ae095de0170421d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233039323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6a1433570c017f9e332bb3da6c5fc56eda15f9ec0090c45b85426f9c85c492`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:12:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:13:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:13:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:13:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4fc43557d62ddd16c656bf04b429b1d3d4242eefbf7376c7bc7157cb6dbc75`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e007b90980b27f2a5c2d23d2805be4fc440f42b0a234e035553f83ce3d655e3`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bd070cd646aa089f2ef70c669e9efd62ecfe9a68599d5a0f9d03cf8b691632`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 5.8 MB (5792121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864694b8117ba3d2e3c796ae5bfc310c64e3b892a30f3154f247c07046456bea`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0839df9247577841d66ffb4ab37613fd589f948d44d202ad9687bd5a871fd3a6`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7dc1e857dfa00f75aae78cb7a5429573ed43e59d2df5f037243de08b07aada`  
		Last Modified: Tue, 12 May 2026 19:13:49 GMT  
		Size: 49.8 MB (49825749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6463de6f8b7165d27c52df2c7c2b48e736918f70ef0549acf45d4dc2d00a2`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fadccec8f2daadad930e82a7556cd1aa0c890fa5a5badf033a646af1e84963`  
		Last Modified: Tue, 12 May 2026 19:13:56 GMT  
		Size: 130.8 MB (130775477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2193cf3f7597227ae8ea8c800711e55fad5964a1b3d5842223de41786572914`  
		Last Modified: Tue, 12 May 2026 19:13:48 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:96d3713d71ba400559341758e67f9aaf6de60b4ad080c1ee2839f6a95f3ac13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19386f1b3cbf6dffacb1557db1e5e8034a0cc77a5ccfe062ee5830141121d60f`

```dockerfile
```

-	Layers:
	-	`sha256:b0a38a345e943e2ce8d6374bd4b28d6a22dc7df32e8a3a18bff449dfa10ce12a`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5915ffd95d6625c09bb4c7754a4280a85a3b569a6e5f763c2024fea2602498aa`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:c36050afdca850f23cef85703f84c7531a5ae155a11b5ee1c60acb09937c4084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:14690274f4967ba207939c97dd79a8d6604f1d532218ea6be69c0001ddd2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238253989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1487abffa4fa011710f99e5ae2135537a5f894b7eb1380758b8915884df00e0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148eeb1a828940b6e73c890fece2c98ed8bae18635264f5a16b1353b270b5f6`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bae0286aad01d0c4e14106715011400a75f600841f3717aea2c37e462cb40c`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b1a26b51696a808ea290d78c15b586ded50d5336a9e01494a64ce4135f149b`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 6.2 MB (6170671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab549d4e00e74fbb817c909385b84887c8e3d6fc648ecdba041a510235104380`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90c44920b4ab505625930d4b6e03fdaf4f82cc28f173bfbebe273dcc3746de`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865e9f32c411ea5061231113c45a14007b4d8ba864b130d88383cf0a5231c64`  
		Last Modified: Tue, 12 May 2026 19:13:19 GMT  
		Size: 51.6 MB (51578851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b9b45fc65df7932d8232474d621e9d8ed093e481f4eecb2e9b4d94110efef`  
		Last Modified: Tue, 12 May 2026 19:13:17 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63892f528d32bf597984b4ab748e4743b95af162367aad7f59cbc0a3e0f431fc`  
		Last Modified: Tue, 12 May 2026 19:13:21 GMT  
		Size: 132.4 MB (132401957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6fc0eea0c90041e5698fa8524360c61ccfd4eca8b6c5bf7b19dda35ec150c`  
		Last Modified: Tue, 12 May 2026 19:13:18 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ad2658b0203b3293805fa34fdfd24f6bcc5a0948e3d9bb03f01a60b42470c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46531aada87d2b105c22501c39728fa17fd6ea029ae07d0e1f4a323d62e3370e`

```dockerfile
```

-	Layers:
	-	`sha256:eb33bcfe45069ebd909020642befd333a449c8aea70239d9922fcf983e41c0be`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf9b0caf1546e3a1acae0a554491614c4a1431099e8ba1f92391c08ff6d7a3`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 33.3 KB (33298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c3d0492f593ef24dad1d77ff63bc287041d1d07de5fbc38ae095de0170421d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233039323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6a1433570c017f9e332bb3da6c5fc56eda15f9ec0090c45b85426f9c85c492`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:12:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:13:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:13:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:13:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4fc43557d62ddd16c656bf04b429b1d3d4242eefbf7376c7bc7157cb6dbc75`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e007b90980b27f2a5c2d23d2805be4fc440f42b0a234e035553f83ce3d655e3`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bd070cd646aa089f2ef70c669e9efd62ecfe9a68599d5a0f9d03cf8b691632`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 5.8 MB (5792121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864694b8117ba3d2e3c796ae5bfc310c64e3b892a30f3154f247c07046456bea`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0839df9247577841d66ffb4ab37613fd589f948d44d202ad9687bd5a871fd3a6`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7dc1e857dfa00f75aae78cb7a5429573ed43e59d2df5f037243de08b07aada`  
		Last Modified: Tue, 12 May 2026 19:13:49 GMT  
		Size: 49.8 MB (49825749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6463de6f8b7165d27c52df2c7c2b48e736918f70ef0549acf45d4dc2d00a2`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fadccec8f2daadad930e82a7556cd1aa0c890fa5a5badf033a646af1e84963`  
		Last Modified: Tue, 12 May 2026 19:13:56 GMT  
		Size: 130.8 MB (130775477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2193cf3f7597227ae8ea8c800711e55fad5964a1b3d5842223de41786572914`  
		Last Modified: Tue, 12 May 2026 19:13:48 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:96d3713d71ba400559341758e67f9aaf6de60b4ad080c1ee2839f6a95f3ac13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19386f1b3cbf6dffacb1557db1e5e8034a0cc77a5ccfe062ee5830141121d60f`

```dockerfile
```

-	Layers:
	-	`sha256:b0a38a345e943e2ce8d6374bd4b28d6a22dc7df32e8a3a18bff449dfa10ce12a`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5915ffd95d6625c09bb4c7754a4280a85a3b569a6e5f763c2024fea2602498aa`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:c36050afdca850f23cef85703f84c7531a5ae155a11b5ee1c60acb09937c4084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:14690274f4967ba207939c97dd79a8d6604f1d532218ea6be69c0001ddd2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238253989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1487abffa4fa011710f99e5ae2135537a5f894b7eb1380758b8915884df00e0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148eeb1a828940b6e73c890fece2c98ed8bae18635264f5a16b1353b270b5f6`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bae0286aad01d0c4e14106715011400a75f600841f3717aea2c37e462cb40c`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b1a26b51696a808ea290d78c15b586ded50d5336a9e01494a64ce4135f149b`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 6.2 MB (6170671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab549d4e00e74fbb817c909385b84887c8e3d6fc648ecdba041a510235104380`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90c44920b4ab505625930d4b6e03fdaf4f82cc28f173bfbebe273dcc3746de`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865e9f32c411ea5061231113c45a14007b4d8ba864b130d88383cf0a5231c64`  
		Last Modified: Tue, 12 May 2026 19:13:19 GMT  
		Size: 51.6 MB (51578851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b9b45fc65df7932d8232474d621e9d8ed093e481f4eecb2e9b4d94110efef`  
		Last Modified: Tue, 12 May 2026 19:13:17 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63892f528d32bf597984b4ab748e4743b95af162367aad7f59cbc0a3e0f431fc`  
		Last Modified: Tue, 12 May 2026 19:13:21 GMT  
		Size: 132.4 MB (132401957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6fc0eea0c90041e5698fa8524360c61ccfd4eca8b6c5bf7b19dda35ec150c`  
		Last Modified: Tue, 12 May 2026 19:13:18 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:ad2658b0203b3293805fa34fdfd24f6bcc5a0948e3d9bb03f01a60b42470c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46531aada87d2b105c22501c39728fa17fd6ea029ae07d0e1f4a323d62e3370e`

```dockerfile
```

-	Layers:
	-	`sha256:eb33bcfe45069ebd909020642befd333a449c8aea70239d9922fcf983e41c0be`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf9b0caf1546e3a1acae0a554491614c4a1431099e8ba1f92391c08ff6d7a3`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 33.3 KB (33298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c3d0492f593ef24dad1d77ff63bc287041d1d07de5fbc38ae095de0170421d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233039323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6a1433570c017f9e332bb3da6c5fc56eda15f9ec0090c45b85426f9c85c492`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:12:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:13:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:13:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:13:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4fc43557d62ddd16c656bf04b429b1d3d4242eefbf7376c7bc7157cb6dbc75`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e007b90980b27f2a5c2d23d2805be4fc440f42b0a234e035553f83ce3d655e3`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bd070cd646aa089f2ef70c669e9efd62ecfe9a68599d5a0f9d03cf8b691632`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 5.8 MB (5792121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864694b8117ba3d2e3c796ae5bfc310c64e3b892a30f3154f247c07046456bea`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0839df9247577841d66ffb4ab37613fd589f948d44d202ad9687bd5a871fd3a6`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7dc1e857dfa00f75aae78cb7a5429573ed43e59d2df5f037243de08b07aada`  
		Last Modified: Tue, 12 May 2026 19:13:49 GMT  
		Size: 49.8 MB (49825749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6463de6f8b7165d27c52df2c7c2b48e736918f70ef0549acf45d4dc2d00a2`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fadccec8f2daadad930e82a7556cd1aa0c890fa5a5badf033a646af1e84963`  
		Last Modified: Tue, 12 May 2026 19:13:56 GMT  
		Size: 130.8 MB (130775477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2193cf3f7597227ae8ea8c800711e55fad5964a1b3d5842223de41786572914`  
		Last Modified: Tue, 12 May 2026 19:13:48 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:96d3713d71ba400559341758e67f9aaf6de60b4ad080c1ee2839f6a95f3ac13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19386f1b3cbf6dffacb1557db1e5e8034a0cc77a5ccfe062ee5830141121d60f`

```dockerfile
```

-	Layers:
	-	`sha256:b0a38a345e943e2ce8d6374bd4b28d6a22dc7df32e8a3a18bff449dfa10ce12a`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5915ffd95d6625c09bb4c7754a4280a85a3b569a6e5f763c2024fea2602498aa`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:c36050afdca850f23cef85703f84c7531a5ae155a11b5ee1c60acb09937c4084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:14690274f4967ba207939c97dd79a8d6604f1d532218ea6be69c0001ddd2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238253989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1487abffa4fa011710f99e5ae2135537a5f894b7eb1380758b8915884df00e0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148eeb1a828940b6e73c890fece2c98ed8bae18635264f5a16b1353b270b5f6`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bae0286aad01d0c4e14106715011400a75f600841f3717aea2c37e462cb40c`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b1a26b51696a808ea290d78c15b586ded50d5336a9e01494a64ce4135f149b`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 6.2 MB (6170671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab549d4e00e74fbb817c909385b84887c8e3d6fc648ecdba041a510235104380`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90c44920b4ab505625930d4b6e03fdaf4f82cc28f173bfbebe273dcc3746de`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865e9f32c411ea5061231113c45a14007b4d8ba864b130d88383cf0a5231c64`  
		Last Modified: Tue, 12 May 2026 19:13:19 GMT  
		Size: 51.6 MB (51578851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b9b45fc65df7932d8232474d621e9d8ed093e481f4eecb2e9b4d94110efef`  
		Last Modified: Tue, 12 May 2026 19:13:17 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63892f528d32bf597984b4ab748e4743b95af162367aad7f59cbc0a3e0f431fc`  
		Last Modified: Tue, 12 May 2026 19:13:21 GMT  
		Size: 132.4 MB (132401957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6fc0eea0c90041e5698fa8524360c61ccfd4eca8b6c5bf7b19dda35ec150c`  
		Last Modified: Tue, 12 May 2026 19:13:18 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad2658b0203b3293805fa34fdfd24f6bcc5a0948e3d9bb03f01a60b42470c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46531aada87d2b105c22501c39728fa17fd6ea029ae07d0e1f4a323d62e3370e`

```dockerfile
```

-	Layers:
	-	`sha256:eb33bcfe45069ebd909020642befd333a449c8aea70239d9922fcf983e41c0be`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf9b0caf1546e3a1acae0a554491614c4a1431099e8ba1f92391c08ff6d7a3`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 33.3 KB (33298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c3d0492f593ef24dad1d77ff63bc287041d1d07de5fbc38ae095de0170421d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233039323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6a1433570c017f9e332bb3da6c5fc56eda15f9ec0090c45b85426f9c85c492`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:12:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:13:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:13:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:13:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4fc43557d62ddd16c656bf04b429b1d3d4242eefbf7376c7bc7157cb6dbc75`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e007b90980b27f2a5c2d23d2805be4fc440f42b0a234e035553f83ce3d655e3`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bd070cd646aa089f2ef70c669e9efd62ecfe9a68599d5a0f9d03cf8b691632`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 5.8 MB (5792121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864694b8117ba3d2e3c796ae5bfc310c64e3b892a30f3154f247c07046456bea`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0839df9247577841d66ffb4ab37613fd589f948d44d202ad9687bd5a871fd3a6`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7dc1e857dfa00f75aae78cb7a5429573ed43e59d2df5f037243de08b07aada`  
		Last Modified: Tue, 12 May 2026 19:13:49 GMT  
		Size: 49.8 MB (49825749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6463de6f8b7165d27c52df2c7c2b48e736918f70ef0549acf45d4dc2d00a2`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fadccec8f2daadad930e82a7556cd1aa0c890fa5a5badf033a646af1e84963`  
		Last Modified: Tue, 12 May 2026 19:13:56 GMT  
		Size: 130.8 MB (130775477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2193cf3f7597227ae8ea8c800711e55fad5964a1b3d5842223de41786572914`  
		Last Modified: Tue, 12 May 2026 19:13:48 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:96d3713d71ba400559341758e67f9aaf6de60b4ad080c1ee2839f6a95f3ac13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19386f1b3cbf6dffacb1557db1e5e8034a0cc77a5ccfe062ee5830141121d60f`

```dockerfile
```

-	Layers:
	-	`sha256:b0a38a345e943e2ce8d6374bd4b28d6a22dc7df32e8a3a18bff449dfa10ce12a`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5915ffd95d6625c09bb4c7754a4280a85a3b569a6e5f763c2024fea2602498aa`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:c36050afdca850f23cef85703f84c7531a5ae155a11b5ee1c60acb09937c4084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:14690274f4967ba207939c97dd79a8d6604f1d532218ea6be69c0001ddd2d45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238253989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1487abffa4fa011710f99e5ae2135537a5f894b7eb1380758b8915884df00e0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:11:33 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:11:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:04 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:04 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:43 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148eeb1a828940b6e73c890fece2c98ed8bae18635264f5a16b1353b270b5f6`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bae0286aad01d0c4e14106715011400a75f600841f3717aea2c37e462cb40c`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b1a26b51696a808ea290d78c15b586ded50d5336a9e01494a64ce4135f149b`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 6.2 MB (6170671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab549d4e00e74fbb817c909385b84887c8e3d6fc648ecdba041a510235104380`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90c44920b4ab505625930d4b6e03fdaf4f82cc28f173bfbebe273dcc3746de`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865e9f32c411ea5061231113c45a14007b4d8ba864b130d88383cf0a5231c64`  
		Last Modified: Tue, 12 May 2026 19:13:19 GMT  
		Size: 51.6 MB (51578851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b9b45fc65df7932d8232474d621e9d8ed093e481f4eecb2e9b4d94110efef`  
		Last Modified: Tue, 12 May 2026 19:13:17 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63892f528d32bf597984b4ab748e4743b95af162367aad7f59cbc0a3e0f431fc`  
		Last Modified: Tue, 12 May 2026 19:13:21 GMT  
		Size: 132.4 MB (132401957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f6fc0eea0c90041e5698fa8524360c61ccfd4eca8b6c5bf7b19dda35ec150c`  
		Last Modified: Tue, 12 May 2026 19:13:18 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ad2658b0203b3293805fa34fdfd24f6bcc5a0948e3d9bb03f01a60b42470c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46531aada87d2b105c22501c39728fa17fd6ea029ae07d0e1f4a323d62e3370e`

```dockerfile
```

-	Layers:
	-	`sha256:eb33bcfe45069ebd909020642befd333a449c8aea70239d9922fcf983e41c0be`  
		Last Modified: Tue, 12 May 2026 19:13:16 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf9b0caf1546e3a1acae0a554491614c4a1431099e8ba1f92391c08ff6d7a3`  
		Last Modified: Tue, 12 May 2026 19:13:15 GMT  
		Size: 33.3 KB (33298 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:c3d0492f593ef24dad1d77ff63bc287041d1d07de5fbc38ae095de0170421d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233039323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6a1433570c017f9e332bb3da6c5fc56eda15f9ec0090c45b85426f9c85c492`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:11:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:11:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:12:02 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 12 May 2026 19:12:03 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:12:03 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:12:35 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:12:35 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Tue, 12 May 2026 19:13:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:13:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:13:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:13:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:13:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:13:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4fc43557d62ddd16c656bf04b429b1d3d4242eefbf7376c7bc7157cb6dbc75`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e007b90980b27f2a5c2d23d2805be4fc440f42b0a234e035553f83ce3d655e3`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bd070cd646aa089f2ef70c669e9efd62ecfe9a68599d5a0f9d03cf8b691632`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 5.8 MB (5792121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864694b8117ba3d2e3c796ae5bfc310c64e3b892a30f3154f247c07046456bea`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0839df9247577841d66ffb4ab37613fd589f948d44d202ad9687bd5a871fd3a6`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7dc1e857dfa00f75aae78cb7a5429573ed43e59d2df5f037243de08b07aada`  
		Last Modified: Tue, 12 May 2026 19:13:49 GMT  
		Size: 49.8 MB (49825749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6463de6f8b7165d27c52df2c7c2b48e736918f70ef0549acf45d4dc2d00a2`  
		Last Modified: Tue, 12 May 2026 19:13:47 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fadccec8f2daadad930e82a7556cd1aa0c890fa5a5badf033a646af1e84963`  
		Last Modified: Tue, 12 May 2026 19:13:56 GMT  
		Size: 130.8 MB (130775477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2193cf3f7597227ae8ea8c800711e55fad5964a1b3d5842223de41786572914`  
		Last Modified: Tue, 12 May 2026 19:13:48 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:96d3713d71ba400559341758e67f9aaf6de60b4ad080c1ee2839f6a95f3ac13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19386f1b3cbf6dffacb1557db1e5e8034a0cc77a5ccfe062ee5830141121d60f`

```dockerfile
```

-	Layers:
	-	`sha256:b0a38a345e943e2ce8d6374bd4b28d6a22dc7df32e8a3a18bff449dfa10ce12a`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5915ffd95d6625c09bb4c7754a4280a85a3b569a6e5f763c2024fea2602498aa`  
		Last Modified: Tue, 12 May 2026 19:13:46 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.10`

**does not exist** (yet?)

## `mysql:8.4.10-oracle`

**does not exist** (yet?)

## `mysql:8.4.10-oraclelinux9`

**does not exist** (yet?)

## `mysql:9`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7-oracle`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7-oraclelinux9`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.1`

**does not exist** (yet?)

## `mysql:9.7.1-oracle`

**does not exist** (yet?)

## `mysql:9.7.1-oraclelinux9`

**does not exist** (yet?)

## `mysql:latest`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:c11782aa2a96624c1efc121768641d96954faa136d6aa82751b032d8c426ffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f0f0d4591d23106312b3f7fbad8f4062a938a64e3e748c47b8c4347640265182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273445935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094aec64961bf03283c2c3a4dd8805dc3d61ff83dbc37eaabc30d9d3e379449c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:41 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:41 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:14 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:11:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:11:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:11:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:11:57 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:11:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edacfaea72efd985c78636f44f7201731e5469306545bb14f347eda6bdfd06`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f19ed5e677faebb16512046d6c98b4f8c3a0068f650d61356e6a6dfd4ad15`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74943462a4ff484dafcc3f1c121e99a51f207b83363adcf0b110130500953de`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 6.2 MB (6170689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec50bfa3b7ec25102f238db51447707d71c1c34da5fe3b304ce273abe415de3`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35300b480a58c039caef3475555ff5ed522db79d4b070c606cf459666a48daa6`  
		Last Modified: Tue, 12 May 2026 19:12:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491a2a13e1bb9fa0503117c4e29937f354d4aa5b7ba4c12ad7f0c0169e6eea7`  
		Last Modified: Tue, 12 May 2026 19:12:39 GMT  
		Size: 57.0 MB (56969334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b372994e5fba5935c4be8d32f319bba1f1b7574ebd129ea3e48e99672e0d0`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23ccd262062f75641ff194f36799296fa69a59c553e53817ca827dd5e473d3`  
		Last Modified: Tue, 12 May 2026 19:12:44 GMT  
		Size: 162.2 MB (162203403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b6dd0c6bdf7e6aa00c267d2307fd295c7aa6048cd383212a62aefd8d89580`  
		Last Modified: Tue, 12 May 2026 19:12:36 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6ff4662ac78b1775d53e7f1f1afb9ead0211c7ddc0a0e36282d31c13638c283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11ce0de44c21e967f6fb7c7b3a5c0c3b58c840f14bf9835d75c801fb84d9edf`

```dockerfile
```

-	Layers:
	-	`sha256:b3e52f10da63e070831028bf7328c5fb381e39a4425886a74b1f63e322334bf7`  
		Last Modified: Tue, 12 May 2026 19:12:34 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d3f438d99e31cbcfdd17f992f1e0d81a257688704c0b4cf86cd7e85a9577d`  
		Last Modified: Tue, 12 May 2026 19:12:33 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2d43877d4b543ae29100a7cb3a7ad03e983fb5149960ed726693ad59acc11836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269907960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7203987a324be0eeb97d28eb127622fb048ae8980c170049c80d55b9928ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 12 May 2026 19:10:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 12 May 2026 19:10:20 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 19:10:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_MAJOR=9.7
# Tue, 12 May 2026 19:10:56 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:10:56 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 12 May 2026 19:11:30 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 12 May 2026 19:11:30 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Tue, 12 May 2026 19:12:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 12 May 2026 19:12:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 May 2026 19:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 19:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 19:12:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 12 May 2026 19:12:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a13c12c93c1399fb49243c2d736f3021a86ab63049779d5b329c5b5debe26ac`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919faf9eb7be83c84762fe6d5bfccf3e7a7520cf7d23c7b1275849b60ca390`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5770eff9743e9b59443e5782ce6752f077951ba2c212fedb97b42a7643b8e`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 5.8 MB (5792128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2ad1ff17eb84f3ca0d7dff6f31f2455a5d7753b3fdfe740fe556711266d009`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a09fca0124b6e763de7d85a381b7e5ab5c028dcbf7e47df6719d872c3e999ce`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6591e9dc619234c335d80dc5705e98d22e08780a552529d065bddca540b95759`  
		Last Modified: Tue, 12 May 2026 19:12:55 GMT  
		Size: 57.0 MB (56982581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a7551afaf58087d3dcdee63ad5c33e5a62afc507df9752b5b54360edc0339`  
		Last Modified: Tue, 12 May 2026 19:12:52 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e993edb915c5fcbb320984ce5df53244f586c8fe255dfccf17e3726d1ac4ef`  
		Last Modified: Tue, 12 May 2026 19:13:00 GMT  
		Size: 160.5 MB (160487270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a0c748a764489dceb7f2e274c98312f1a3ffb8e7b07fd7b9a2cf72e6aeb579`  
		Last Modified: Tue, 12 May 2026 19:12:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:90278206f83f7b293c73ad9fd5232586688cdf9fa15cf4787671c1a078e88bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0cfccaae9969b7fa15581e52410aea64bba6710a75589ac2098f663f8f954d`

```dockerfile
```

-	Layers:
	-	`sha256:f89612214b00ce151bb66634a2c23ae33fa54b6ebe48b860996be8ed1cc43b1c`  
		Last Modified: Tue, 12 May 2026 19:12:51 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba395b333a7d234ebd78621462aba8dae5f2e1e84d644a2f32648a2ba97733a`  
		Last Modified: Tue, 12 May 2026 19:12:50 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json
