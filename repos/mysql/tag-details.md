<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux9`](#mysql8-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.9`](#mysql849)
-	[`mysql:8.4.9-oracle`](#mysql849-oracle)
-	[`mysql:8.4.9-oraclelinux9`](#mysql849-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.7`](#mysql97)
-	[`mysql:9.7-oracle`](#mysql97-oracle)
-	[`mysql:9.7-oraclelinux9`](#mysql97-oraclelinux9)
-	[`mysql:9.7.0`](#mysql970)
-	[`mysql:9.7.0-oracle`](#mysql970-oracle)
-	[`mysql:9.7.0-oraclelinux9`](#mysql970-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.9`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.9` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.9-oracle`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.9-oraclelinux9`

```console
$ docker pull mysql@sha256:21d5c55b7f74a97dcbd281dfbb10356a16b1199da956a63b55493418afe2b940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:fb2cf554aae5a4afdbed0a2b1c43e722bd61b8f64c372b5059bccc96c0cc2d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238260610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d1e47c5714526f5467c50c6c3969743660f2bcf01de642033de8792c1802a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:58:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:58:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:58:53 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 22:59:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:59:28 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:59:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:59:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:59:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528ed92354da0a79023d375e777c76fa561888360242ee0e687923106b7b1ec`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb083db72a6e8a3ae8607518353b85ae3ca011791cc42f513da82d87211df4a`  
		Last Modified: Mon, 04 May 2026 22:59:59 GMT  
		Size: 51.6 MB (51580064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab7a201068e646861557a725fb5848021ca92895c505650396696b270374fb`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a995cd42599af8b86f7f6c55c44033f8e2e348e7917c4ecec6613a6e2a1f871a`  
		Last Modified: Mon, 04 May 2026 23:00:01 GMT  
		Size: 132.4 MB (132404627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96eb2c38e0f2c4b35cee92647fb28d8acc80e23c5fcc69d80fad91474012584`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d5de83be11cd5255becceb214a41404e933d152d8d39e396f6e84d8f90cfefe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1736acb6099e9dae96630a4df4cb49b991cb974c3b525a949e6c12f6779e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:46e91b60ed0216f1ae08eac51e0249396334f0bd96bca489bdce71353a317757`  
		Last Modified: Mon, 04 May 2026 22:59:58 GMT  
		Size: 15.7 MB (15710006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b19d1ea67dfc707d631a4a23250639db716c40500304c3d2a7eba37b8819899`  
		Last Modified: Mon, 04 May 2026 22:59:57 GMT  
		Size: 33.3 KB (33297 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:871812bb5e91918c23410ecc4aa22c5e39b7c84e12cf52c231ef3dcca82c7490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233045781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a23f791babc29afc73f7aac77970fa302d5d219a30f7bd487875fac0fa61a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:00 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:09:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:09:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.9-1.el9
# Mon, 04 May 2026 21:10:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1bc55eb16e754134bfba815453a74ba93ea6bbd9d27ac316b2b77850577bd`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2128c976b29d78f69a41ad76dc67cce8fd800a52d130d6f8293579fcd1eeda7`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 737.5 KB (737523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3bb1d63c466ebaa0fc2e8398cc873848a023facf67ba0dcccfc681aa5100f`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 5.8 MB (5790759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425b0dd192e6ec77f0ad5828754df7a0c1a628f687c6403042a8fc57afe9526`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c472e44f6b5ea3845f0e830eb674735904ec11a653cb994eb1a75e7c56ef91`  
		Last Modified: Mon, 04 May 2026 21:11:13 GMT  
		Size: 49.8 MB (49827931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcfe4c9099b1ca747e6e5acb104014cb0296556d10ee53f5089cf1375fac04`  
		Last Modified: Mon, 04 May 2026 21:11:11 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a675bd3a34fe3e962a1f6831dac4f2a176cf88ef1c315ddf72c8ddfc4cf7cf`  
		Last Modified: Mon, 04 May 2026 21:11:14 GMT  
		Size: 130.8 MB (130781172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c228476154cbed5491d4e3a805938f4c9c72a02a71b23ba559be75b16d8353`  
		Last Modified: Mon, 04 May 2026 21:11:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:18c43f282a55b36187af012ed452a1d4e96c3285030f724f6b09f44a1fbb8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15741957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49528778add127479f721d7f18c2e08febbe37f5966bcc0ed2e838f8839c90fa`

```dockerfile
```

-	Layers:
	-	`sha256:bf9d312db6bf9479e660fae507ac8fc00fa4b0e7c065fa2550a97941ff5cd192`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 15.7 MB (15708390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22236123f06da452f975f4518ee91c8b7e0af5875ec06e7f0cb73818131b00a2`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 33.6 KB (33567 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7-oracle`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7-oraclelinux9`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.0`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.0` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.0-oracle`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.7.0-oraclelinux9`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.7.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.7.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.7.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:cf40d2c53b86849a8d31bc5784d74a7c3a7b5545f4e5d67691ce8fa19dbf080b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:73bef09b4eff904595e1a9924b42403866b614e93d89777052b3e8b2d031d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273462580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47cf584580a92069b6d5701b283414e7ce62423c8a1e298c36ab64bb756c1c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:56:02 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:56:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:56:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 22:56:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 22:56:30 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:56:30 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 22:56:58 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 22:56:58 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 22:57:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 22:57:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 22:57:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 22:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 22:57:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 22:57:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91119dbf849e9fb34f796f02c8350c3ee011aa75181b88edc82371e8ef55000f`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34fede4754824f3c114ed9f3547d8526445f4305c12341c666b78f3ace8bd2`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946e9b141a33eb6fb0762e5522d6fd8d9d1a16c85ea6aabdc8956915302f84de`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 6.2 MB (6173030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7640bc9e91df29c2d9dbf72d084def91d6e07dbefbab1ec9eb4c42d39990770b`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaefa41872fe8c8f053bbfccd8101ff7f57921e86153e60963b8fb1350d5e32`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baa88ab2f91d34eff9f83f9ed84c85b035c1e46a5faf25b04f4fd40893a9b9`  
		Last Modified: Mon, 04 May 2026 22:58:17 GMT  
		Size: 57.0 MB (56972890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a595b060d0954bd1e8bf1dc1f75edca9e7ddd60ef146ffa76dde492c0234ca0`  
		Last Modified: Mon, 04 May 2026 22:58:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959718775b8eb2caee5c2228be784d46d7251b1e67b707d95fc10f16ff6d054`  
		Last Modified: Mon, 04 May 2026 22:58:19 GMT  
		Size: 162.2 MB (162213775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e2bf1deee74679314afec1efb4037eb305623d4a3c672fc39a10aba1d4dd`  
		Last Modified: Mon, 04 May 2026 22:58:16 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:51948599d73f6f045402f7bdfecc57a452f01a57b6cd9e7f9f90b81823c912a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16823862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31a0f388d516fd02195eda7902058e2b7926880db220e4e50b780895605524`

```dockerfile
```

-	Layers:
	-	`sha256:c52a7332fb43b620d1766079c7caf45bc9284c3f3d0e1055a3e38888758e94be`  
		Last Modified: Mon, 04 May 2026 22:58:14 GMT  
		Size: 16.8 MB (16788754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19014663b9ecff9b58ae6c562b16755dbd57ed1c13ab78ec09bb74416391c590`  
		Last Modified: Mon, 04 May 2026 22:58:13 GMT  
		Size: 35.1 KB (35108 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2fa34e99773301014cd991ae65b9a4c2e934a4d0403f6eba76e417dab1b8d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442b8db2f20d21031594573141abdbf6a2dd63dbfff4087482d7d1a76c37e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:08:57 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:08:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:08:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_MAJOR=9.7
# Mon, 04 May 2026 21:09:29 GMT
ENV MYSQL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:09:29 GMT
RUN set -eu; 	{ 		echo '[mysql9.7-server-minimal]'; 		echo 'name=MySQL 9.7 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-9.7-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:00 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-9.7-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:00 GMT
ENV MYSQL_SHELL_VERSION=9.7.0-1.el9
# Mon, 04 May 2026 21:10:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:10:44 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:10:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:10:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658cf3809cdf66916d4ae80f9fbdbf2ce418edd07c0c3d9f15c78a98248852b`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d15d4bd606fba07bd48aca9d77b5b11edeb2974d8bac400c8498987f68e2a`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e989ffbf19734c8ef04538b2e50bade50c3110bf0586bd92672d3566424130`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 5.8 MB (5790756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9b3f5c2b4307f1b109e3f3e4c808a35699b3ad4f736574a93aa776f3e7427`  
		Last Modified: Mon, 04 May 2026 21:11:10 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5c90f535adb91b18eacda78a9e62b71e5ba5e0a6fe785a566b1cb1dbe7c4e4`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838d2f46e3df9f2f1b27626c6fe842a8d30523e17bd6bba2c86bdc869deb06f`  
		Last Modified: Mon, 04 May 2026 21:11:24 GMT  
		Size: 57.0 MB (56983090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505aa7f4d7942ecbab4820ec2e34dc8733c5478356c7458c22c40aadd5eb873`  
		Last Modified: Mon, 04 May 2026 21:11:22 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af6d538acbd6e4654372a8dd246d6cee34096a7e99812c1f3416250dd31605`  
		Last Modified: Mon, 04 May 2026 21:11:26 GMT  
		Size: 160.5 MB (160488794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ddb25249c7f44ebc5e90b15ff621d12c3a1397c213e92ef7131ffd3f163f6`  
		Last Modified: Mon, 04 May 2026 21:11:23 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3c60b1dac4c0a1b76ca41c7da7a5a29a7aee5f413642229e7d9158610b8a183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121591fa331c19957701197526c6ee65b99b9c66a9dc3a5a937627ea9f8c1ca6`

```dockerfile
```

-	Layers:
	-	`sha256:d62755c4342059bb85df263aea48b42594129162bbb70379b42b1ba66abcc7b6`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 16.8 MB (16787210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff0ac1686f49579285d64201585ab619c337e630ba98ed1fb47004be03cad17`  
		Last Modified: Mon, 04 May 2026 21:11:21 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json
