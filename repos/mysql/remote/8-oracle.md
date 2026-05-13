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
