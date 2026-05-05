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
-	[`mysql:8.0.46`](#mysql8046)
-	[`mysql:8.0.46-bookworm`](#mysql8046-bookworm)
-	[`mysql:8.0.46-debian`](#mysql8046-debian)
-	[`mysql:8.0.46-oracle`](#mysql8046-oracle)
-	[`mysql:8.0.46-oraclelinux9`](#mysql8046-oraclelinux9)
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

## `mysql:8.0`

```console
$ docker pull mysql@sha256:7dcddc01f13bab2f15cde676d44d01f61fc9f99fe7785e86196dfc07d358ae2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:62fb722c78b24245ddff1796a0fcee4a49cc5b87e0aaaf20c92d1da9e0a2497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233581538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd09145362dfe6831b14545de3d5fd6cc75c37cfd6ef8561429c1fc73518b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:59:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:59:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:59:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 23:00:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:01:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 23:01:20 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 23:01:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 23:01:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 23:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 23:01:20 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 23:01:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6c7b50a938e4f81a40ed970b0a1b4d6409d55032d50c0d8a30042b484226f`  
		Last Modified: Mon, 04 May 2026 23:01:51 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5d1ac74c19e81a17008c972f1ca25e9c4dc509307c3eee1382e7301f0f7a4`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 783.6 KB (783558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74d296605b0eb8f94dd83441a08a413f4ae4f2aafa9e7d1e2da5adcdade645`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 6.2 MB (6173009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297d04cfe4705c95a7d1a6abb5831e3637edfebdb6b639661c8c66ff2220cd64`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a3e0d4e4b216b443a3125ae3f947d8d0e9df399ba4af9bbb5823703c95c1f`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63160a5eda1f2bc97de740813d14908519eba5d1d59da5f7f6934126d33ce17`  
		Last Modified: Mon, 04 May 2026 23:01:55 GMT  
		Size: 49.9 MB (49934187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7534d1db9f8dcc7acdd28f0655c93bd0b045dee128866ff2809c833a6462eaf1`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ec2dab01d93d549839d59c815b48a834beca654fc9d45a86eaddc8fd82cc5a`  
		Last Modified: Mon, 04 May 2026 23:01:57 GMT  
		Size: 129.4 MB (129371339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab24264a27e9ec0085b30b83b81272417504c9e231d006975e9956af3526a3ab`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d30d9fbee877d823d9807f43df6c030983d61d7a645d0f5ac2c7154a8abd12`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:fed8ae184a51c4b7d9cc23dd38a0a1bed605380eb6f11e0f45dd08c2db084d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27122045730314b10f63d94f0d07039b28a4aa531f13ae4b0563f16e3a397235`

```dockerfile
```

-	Layers:
	-	`sha256:af166387641d84cdf7a5b00f7127dcdd3f9829c942fc697d6275e92b331abe0f`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 15.4 MB (15434095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796812c73292ea535203de666541c84fa0203f9ad3a960045dfbb1a55c8cf062`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:213bbfaf699693a40a20a12bb4342d2589a15a3dc7153db698eaed252a92458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229139579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e118f56c5963e079252e0d6e2978c9c010eb7fc7aaaec100e367796b5dd08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:09:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:11:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:11:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:11:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:11:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:11:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a53223cb4cb4f2abbb070ad06dba8b1c95c6deac4666e954d223c97ad0b471`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f24d93d521ecd5f1ede50bb6157f3b19c601ddc22d307b2880b6dddbe03b2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c0b299cb470fda07120beb3b619b655387ec5f4a2da72ce9330d2f194c7029`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 5.8 MB (5790720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce425b17caf10ed18a4d56a89d8a1c078c9fe1c7d3edd22fc45f3c0bd913da2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b2852d2a9df74e94222dd4d151b25ba5397968a479cc85cc31b23041f871a0`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605b7f42ac6ece809a06d59a07fa37ebc3ba9373b1aa1a22966677931451e41a`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 48.8 MB (48787669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1959e4a06a1cc7ddadccce363a91f5bd01ae4f93be2cdbf461f87f2e8529ac81`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa30ab141b5a5b854dbb1adf9111599d6d2b71c8819a1bb1fae8ccd5ee0f7c2c`  
		Last Modified: Mon, 04 May 2026 21:11:49 GMT  
		Size: 127.9 MB (127915155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42505e6e6b9177d92b219bcdfda82f6718e3de57a8bd37ff12c40ccf53db37d8`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcb28d1dfcf6af3f3b0b4cffdb6807ddbb75d4e91ecdae2c33728f0a27214f3`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:9b41c768826231fff8ecb98e1f440b5c1d424c969657458da2b82e85437ec0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0adef218acadd6ab1e34ab53c0140485524c67d6ae8c87f54aa9c14592c3c`

```dockerfile
```

-	Layers:
	-	`sha256:578f543767f02fd88515a88c5d349ea41c6520d836c4ceaf95626a610a89e3ed`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 15.4 MB (15432443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0e30178db86f71b9c37b48b46e426909127768c1fd481ccb7e74423480b9ce`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:9382e4f6f7f013231049ab854de9d0810594d028f4237b67102acc7ade8e3a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:0845b57a4927c2e2e442b0c3c154ebf2bdede7d6e1cb3b5a4b3e8bc1d0e69e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183493846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd5f2526848a17828c97ea713b778389f599988dc03bb40817bbd0f4e8cff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 22 Apr 2026 01:41:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:42:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_VERSION=8.0.46-1debian12
# Wed, 22 Apr 2026 01:42:07 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Apr 2026 01:42:17 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Apr 2026 01:42:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855a4662f4674f4b2fa5b3319559ce3157688e702d8c2a79583f0da1351e556`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8a7b62f21cd8c4c97cd9f0ac47e47d244e51a06b6c9d503173911a5511e0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9904ed9c36af76fad8fec577f30214c654ee4d5b049c97f3bf60a035c596e2`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.2 MB (1248703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223423e03ce3b1462874ffb00ccf06b7d33ccdfaf4ab8d5267d4b1fcb2a3461`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd0e9a8806dfb4190a5efb53b9068f1473ec79c114ae9acf64e04ae785cfd3`  
		Last Modified: Wed, 22 Apr 2026 01:42:42 GMT  
		Size: 15.3 MB (15295542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56737b600a7ed7a14d1e8410aa58f2c34e1a13828090dbb7dbd4fc8a60dba3d`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c65b70c20a21019513cbc8a61d63aa4f5899645c90ecb9f3d2e2151267969e`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2450db828e1da3146b24825caf9ec6f014b7bd17c535dd6aea175bcab19d8`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 134.3 MB (134279198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f61b0173611c4be67c102358804af4fbd8a1c40b8ac915470077320617e17`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908b55f16b6979dab8bf2917860fefd90e59605fc97bf7c1df4914d6d231c81`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4531d449fbdc31a0aa3f36772fc8c521bfa962e70bab3a5abd4d3a4854ac79`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:c3a78f9613889dbaa4d0174c1b5fb8b5cbeb0582a4879cf79141c74c25fa3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f692ec2a7da89ebf2bff1089e62c794c7272afcde68f5f5ad8983acf688d067c`

```dockerfile
```

-	Layers:
	-	`sha256:c864b878b36d1fbfaac5acc28598ccd96160e7d214da4131228041e666b25d0e`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f4d617789ef531659729800ee7388d1c1f154ba9399fae3bbd757f14b5dcc0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:9382e4f6f7f013231049ab854de9d0810594d028f4237b67102acc7ade8e3a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0845b57a4927c2e2e442b0c3c154ebf2bdede7d6e1cb3b5a4b3e8bc1d0e69e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183493846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd5f2526848a17828c97ea713b778389f599988dc03bb40817bbd0f4e8cff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 22 Apr 2026 01:41:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:42:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_VERSION=8.0.46-1debian12
# Wed, 22 Apr 2026 01:42:07 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Apr 2026 01:42:17 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Apr 2026 01:42:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855a4662f4674f4b2fa5b3319559ce3157688e702d8c2a79583f0da1351e556`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8a7b62f21cd8c4c97cd9f0ac47e47d244e51a06b6c9d503173911a5511e0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9904ed9c36af76fad8fec577f30214c654ee4d5b049c97f3bf60a035c596e2`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.2 MB (1248703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223423e03ce3b1462874ffb00ccf06b7d33ccdfaf4ab8d5267d4b1fcb2a3461`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd0e9a8806dfb4190a5efb53b9068f1473ec79c114ae9acf64e04ae785cfd3`  
		Last Modified: Wed, 22 Apr 2026 01:42:42 GMT  
		Size: 15.3 MB (15295542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56737b600a7ed7a14d1e8410aa58f2c34e1a13828090dbb7dbd4fc8a60dba3d`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c65b70c20a21019513cbc8a61d63aa4f5899645c90ecb9f3d2e2151267969e`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2450db828e1da3146b24825caf9ec6f014b7bd17c535dd6aea175bcab19d8`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 134.3 MB (134279198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f61b0173611c4be67c102358804af4fbd8a1c40b8ac915470077320617e17`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908b55f16b6979dab8bf2917860fefd90e59605fc97bf7c1df4914d6d231c81`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4531d449fbdc31a0aa3f36772fc8c521bfa962e70bab3a5abd4d3a4854ac79`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:c3a78f9613889dbaa4d0174c1b5fb8b5cbeb0582a4879cf79141c74c25fa3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f692ec2a7da89ebf2bff1089e62c794c7272afcde68f5f5ad8983acf688d067c`

```dockerfile
```

-	Layers:
	-	`sha256:c864b878b36d1fbfaac5acc28598ccd96160e7d214da4131228041e666b25d0e`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f4d617789ef531659729800ee7388d1c1f154ba9399fae3bbd757f14b5dcc0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:7dcddc01f13bab2f15cde676d44d01f61fc9f99fe7785e86196dfc07d358ae2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:62fb722c78b24245ddff1796a0fcee4a49cc5b87e0aaaf20c92d1da9e0a2497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233581538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd09145362dfe6831b14545de3d5fd6cc75c37cfd6ef8561429c1fc73518b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:59:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:59:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:59:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 23:00:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:01:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 23:01:20 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 23:01:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 23:01:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 23:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 23:01:20 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 23:01:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6c7b50a938e4f81a40ed970b0a1b4d6409d55032d50c0d8a30042b484226f`  
		Last Modified: Mon, 04 May 2026 23:01:51 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5d1ac74c19e81a17008c972f1ca25e9c4dc509307c3eee1382e7301f0f7a4`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 783.6 KB (783558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74d296605b0eb8f94dd83441a08a413f4ae4f2aafa9e7d1e2da5adcdade645`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 6.2 MB (6173009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297d04cfe4705c95a7d1a6abb5831e3637edfebdb6b639661c8c66ff2220cd64`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a3e0d4e4b216b443a3125ae3f947d8d0e9df399ba4af9bbb5823703c95c1f`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63160a5eda1f2bc97de740813d14908519eba5d1d59da5f7f6934126d33ce17`  
		Last Modified: Mon, 04 May 2026 23:01:55 GMT  
		Size: 49.9 MB (49934187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7534d1db9f8dcc7acdd28f0655c93bd0b045dee128866ff2809c833a6462eaf1`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ec2dab01d93d549839d59c815b48a834beca654fc9d45a86eaddc8fd82cc5a`  
		Last Modified: Mon, 04 May 2026 23:01:57 GMT  
		Size: 129.4 MB (129371339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab24264a27e9ec0085b30b83b81272417504c9e231d006975e9956af3526a3ab`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d30d9fbee877d823d9807f43df6c030983d61d7a645d0f5ac2c7154a8abd12`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fed8ae184a51c4b7d9cc23dd38a0a1bed605380eb6f11e0f45dd08c2db084d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27122045730314b10f63d94f0d07039b28a4aa531f13ae4b0563f16e3a397235`

```dockerfile
```

-	Layers:
	-	`sha256:af166387641d84cdf7a5b00f7127dcdd3f9829c942fc697d6275e92b331abe0f`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 15.4 MB (15434095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796812c73292ea535203de666541c84fa0203f9ad3a960045dfbb1a55c8cf062`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:213bbfaf699693a40a20a12bb4342d2589a15a3dc7153db698eaed252a92458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229139579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e118f56c5963e079252e0d6e2978c9c010eb7fc7aaaec100e367796b5dd08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:09:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:11:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:11:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:11:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:11:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:11:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a53223cb4cb4f2abbb070ad06dba8b1c95c6deac4666e954d223c97ad0b471`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f24d93d521ecd5f1ede50bb6157f3b19c601ddc22d307b2880b6dddbe03b2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c0b299cb470fda07120beb3b619b655387ec5f4a2da72ce9330d2f194c7029`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 5.8 MB (5790720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce425b17caf10ed18a4d56a89d8a1c078c9fe1c7d3edd22fc45f3c0bd913da2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b2852d2a9df74e94222dd4d151b25ba5397968a479cc85cc31b23041f871a0`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605b7f42ac6ece809a06d59a07fa37ebc3ba9373b1aa1a22966677931451e41a`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 48.8 MB (48787669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1959e4a06a1cc7ddadccce363a91f5bd01ae4f93be2cdbf461f87f2e8529ac81`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa30ab141b5a5b854dbb1adf9111599d6d2b71c8819a1bb1fae8ccd5ee0f7c2c`  
		Last Modified: Mon, 04 May 2026 21:11:49 GMT  
		Size: 127.9 MB (127915155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42505e6e6b9177d92b219bcdfda82f6718e3de57a8bd37ff12c40ccf53db37d8`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcb28d1dfcf6af3f3b0b4cffdb6807ddbb75d4e91ecdae2c33728f0a27214f3`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9b41c768826231fff8ecb98e1f440b5c1d424c969657458da2b82e85437ec0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0adef218acadd6ab1e34ab53c0140485524c67d6ae8c87f54aa9c14592c3c`

```dockerfile
```

-	Layers:
	-	`sha256:578f543767f02fd88515a88c5d349ea41c6520d836c4ceaf95626a610a89e3ed`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 15.4 MB (15432443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0e30178db86f71b9c37b48b46e426909127768c1fd481ccb7e74423480b9ce`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:7dcddc01f13bab2f15cde676d44d01f61fc9f99fe7785e86196dfc07d358ae2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:62fb722c78b24245ddff1796a0fcee4a49cc5b87e0aaaf20c92d1da9e0a2497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233581538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd09145362dfe6831b14545de3d5fd6cc75c37cfd6ef8561429c1fc73518b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:59:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:59:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:59:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 23:00:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:01:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 23:01:20 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 23:01:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 23:01:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 23:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 23:01:20 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 23:01:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6c7b50a938e4f81a40ed970b0a1b4d6409d55032d50c0d8a30042b484226f`  
		Last Modified: Mon, 04 May 2026 23:01:51 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5d1ac74c19e81a17008c972f1ca25e9c4dc509307c3eee1382e7301f0f7a4`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 783.6 KB (783558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74d296605b0eb8f94dd83441a08a413f4ae4f2aafa9e7d1e2da5adcdade645`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 6.2 MB (6173009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297d04cfe4705c95a7d1a6abb5831e3637edfebdb6b639661c8c66ff2220cd64`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a3e0d4e4b216b443a3125ae3f947d8d0e9df399ba4af9bbb5823703c95c1f`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63160a5eda1f2bc97de740813d14908519eba5d1d59da5f7f6934126d33ce17`  
		Last Modified: Mon, 04 May 2026 23:01:55 GMT  
		Size: 49.9 MB (49934187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7534d1db9f8dcc7acdd28f0655c93bd0b045dee128866ff2809c833a6462eaf1`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ec2dab01d93d549839d59c815b48a834beca654fc9d45a86eaddc8fd82cc5a`  
		Last Modified: Mon, 04 May 2026 23:01:57 GMT  
		Size: 129.4 MB (129371339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab24264a27e9ec0085b30b83b81272417504c9e231d006975e9956af3526a3ab`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d30d9fbee877d823d9807f43df6c030983d61d7a645d0f5ac2c7154a8abd12`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fed8ae184a51c4b7d9cc23dd38a0a1bed605380eb6f11e0f45dd08c2db084d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27122045730314b10f63d94f0d07039b28a4aa531f13ae4b0563f16e3a397235`

```dockerfile
```

-	Layers:
	-	`sha256:af166387641d84cdf7a5b00f7127dcdd3f9829c942fc697d6275e92b331abe0f`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 15.4 MB (15434095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796812c73292ea535203de666541c84fa0203f9ad3a960045dfbb1a55c8cf062`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:213bbfaf699693a40a20a12bb4342d2589a15a3dc7153db698eaed252a92458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229139579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e118f56c5963e079252e0d6e2978c9c010eb7fc7aaaec100e367796b5dd08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:09:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:11:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:11:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:11:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:11:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:11:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a53223cb4cb4f2abbb070ad06dba8b1c95c6deac4666e954d223c97ad0b471`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f24d93d521ecd5f1ede50bb6157f3b19c601ddc22d307b2880b6dddbe03b2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c0b299cb470fda07120beb3b619b655387ec5f4a2da72ce9330d2f194c7029`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 5.8 MB (5790720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce425b17caf10ed18a4d56a89d8a1c078c9fe1c7d3edd22fc45f3c0bd913da2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b2852d2a9df74e94222dd4d151b25ba5397968a479cc85cc31b23041f871a0`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605b7f42ac6ece809a06d59a07fa37ebc3ba9373b1aa1a22966677931451e41a`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 48.8 MB (48787669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1959e4a06a1cc7ddadccce363a91f5bd01ae4f93be2cdbf461f87f2e8529ac81`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa30ab141b5a5b854dbb1adf9111599d6d2b71c8819a1bb1fae8ccd5ee0f7c2c`  
		Last Modified: Mon, 04 May 2026 21:11:49 GMT  
		Size: 127.9 MB (127915155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42505e6e6b9177d92b219bcdfda82f6718e3de57a8bd37ff12c40ccf53db37d8`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcb28d1dfcf6af3f3b0b4cffdb6807ddbb75d4e91ecdae2c33728f0a27214f3`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9b41c768826231fff8ecb98e1f440b5c1d424c969657458da2b82e85437ec0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0adef218acadd6ab1e34ab53c0140485524c67d6ae8c87f54aa9c14592c3c`

```dockerfile
```

-	Layers:
	-	`sha256:578f543767f02fd88515a88c5d349ea41c6520d836c4ceaf95626a610a89e3ed`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 15.4 MB (15432443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0e30178db86f71b9c37b48b46e426909127768c1fd481ccb7e74423480b9ce`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46`

```console
$ docker pull mysql@sha256:7dcddc01f13bab2f15cde676d44d01f61fc9f99fe7785e86196dfc07d358ae2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.46` - linux; amd64

```console
$ docker pull mysql@sha256:62fb722c78b24245ddff1796a0fcee4a49cc5b87e0aaaf20c92d1da9e0a2497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233581538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd09145362dfe6831b14545de3d5fd6cc75c37cfd6ef8561429c1fc73518b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:59:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:59:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:59:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 23:00:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:01:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 23:01:20 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 23:01:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 23:01:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 23:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 23:01:20 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 23:01:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6c7b50a938e4f81a40ed970b0a1b4d6409d55032d50c0d8a30042b484226f`  
		Last Modified: Mon, 04 May 2026 23:01:51 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5d1ac74c19e81a17008c972f1ca25e9c4dc509307c3eee1382e7301f0f7a4`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 783.6 KB (783558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74d296605b0eb8f94dd83441a08a413f4ae4f2aafa9e7d1e2da5adcdade645`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 6.2 MB (6173009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297d04cfe4705c95a7d1a6abb5831e3637edfebdb6b639661c8c66ff2220cd64`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a3e0d4e4b216b443a3125ae3f947d8d0e9df399ba4af9bbb5823703c95c1f`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63160a5eda1f2bc97de740813d14908519eba5d1d59da5f7f6934126d33ce17`  
		Last Modified: Mon, 04 May 2026 23:01:55 GMT  
		Size: 49.9 MB (49934187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7534d1db9f8dcc7acdd28f0655c93bd0b045dee128866ff2809c833a6462eaf1`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ec2dab01d93d549839d59c815b48a834beca654fc9d45a86eaddc8fd82cc5a`  
		Last Modified: Mon, 04 May 2026 23:01:57 GMT  
		Size: 129.4 MB (129371339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab24264a27e9ec0085b30b83b81272417504c9e231d006975e9956af3526a3ab`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d30d9fbee877d823d9807f43df6c030983d61d7a645d0f5ac2c7154a8abd12`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46` - unknown; unknown

```console
$ docker pull mysql@sha256:fed8ae184a51c4b7d9cc23dd38a0a1bed605380eb6f11e0f45dd08c2db084d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27122045730314b10f63d94f0d07039b28a4aa531f13ae4b0563f16e3a397235`

```dockerfile
```

-	Layers:
	-	`sha256:af166387641d84cdf7a5b00f7127dcdd3f9829c942fc697d6275e92b331abe0f`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 15.4 MB (15434095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796812c73292ea535203de666541c84fa0203f9ad3a960045dfbb1a55c8cf062`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.46` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:213bbfaf699693a40a20a12bb4342d2589a15a3dc7153db698eaed252a92458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229139579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e118f56c5963e079252e0d6e2978c9c010eb7fc7aaaec100e367796b5dd08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:09:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:11:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:11:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:11:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:11:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:11:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a53223cb4cb4f2abbb070ad06dba8b1c95c6deac4666e954d223c97ad0b471`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f24d93d521ecd5f1ede50bb6157f3b19c601ddc22d307b2880b6dddbe03b2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c0b299cb470fda07120beb3b619b655387ec5f4a2da72ce9330d2f194c7029`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 5.8 MB (5790720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce425b17caf10ed18a4d56a89d8a1c078c9fe1c7d3edd22fc45f3c0bd913da2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b2852d2a9df74e94222dd4d151b25ba5397968a479cc85cc31b23041f871a0`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605b7f42ac6ece809a06d59a07fa37ebc3ba9373b1aa1a22966677931451e41a`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 48.8 MB (48787669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1959e4a06a1cc7ddadccce363a91f5bd01ae4f93be2cdbf461f87f2e8529ac81`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa30ab141b5a5b854dbb1adf9111599d6d2b71c8819a1bb1fae8ccd5ee0f7c2c`  
		Last Modified: Mon, 04 May 2026 21:11:49 GMT  
		Size: 127.9 MB (127915155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42505e6e6b9177d92b219bcdfda82f6718e3de57a8bd37ff12c40ccf53db37d8`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcb28d1dfcf6af3f3b0b4cffdb6807ddbb75d4e91ecdae2c33728f0a27214f3`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46` - unknown; unknown

```console
$ docker pull mysql@sha256:9b41c768826231fff8ecb98e1f440b5c1d424c969657458da2b82e85437ec0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0adef218acadd6ab1e34ab53c0140485524c67d6ae8c87f54aa9c14592c3c`

```dockerfile
```

-	Layers:
	-	`sha256:578f543767f02fd88515a88c5d349ea41c6520d836c4ceaf95626a610a89e3ed`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 15.4 MB (15432443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0e30178db86f71b9c37b48b46e426909127768c1fd481ccb7e74423480b9ce`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46-bookworm`

```console
$ docker pull mysql@sha256:9382e4f6f7f013231049ab854de9d0810594d028f4237b67102acc7ade8e3a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.46-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:0845b57a4927c2e2e442b0c3c154ebf2bdede7d6e1cb3b5a4b3e8bc1d0e69e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183493846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd5f2526848a17828c97ea713b778389f599988dc03bb40817bbd0f4e8cff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 22 Apr 2026 01:41:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:42:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_VERSION=8.0.46-1debian12
# Wed, 22 Apr 2026 01:42:07 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Apr 2026 01:42:17 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Apr 2026 01:42:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855a4662f4674f4b2fa5b3319559ce3157688e702d8c2a79583f0da1351e556`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8a7b62f21cd8c4c97cd9f0ac47e47d244e51a06b6c9d503173911a5511e0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9904ed9c36af76fad8fec577f30214c654ee4d5b049c97f3bf60a035c596e2`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.2 MB (1248703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223423e03ce3b1462874ffb00ccf06b7d33ccdfaf4ab8d5267d4b1fcb2a3461`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd0e9a8806dfb4190a5efb53b9068f1473ec79c114ae9acf64e04ae785cfd3`  
		Last Modified: Wed, 22 Apr 2026 01:42:42 GMT  
		Size: 15.3 MB (15295542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56737b600a7ed7a14d1e8410aa58f2c34e1a13828090dbb7dbd4fc8a60dba3d`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c65b70c20a21019513cbc8a61d63aa4f5899645c90ecb9f3d2e2151267969e`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2450db828e1da3146b24825caf9ec6f014b7bd17c535dd6aea175bcab19d8`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 134.3 MB (134279198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f61b0173611c4be67c102358804af4fbd8a1c40b8ac915470077320617e17`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908b55f16b6979dab8bf2917860fefd90e59605fc97bf7c1df4914d6d231c81`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4531d449fbdc31a0aa3f36772fc8c521bfa962e70bab3a5abd4d3a4854ac79`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:c3a78f9613889dbaa4d0174c1b5fb8b5cbeb0582a4879cf79141c74c25fa3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f692ec2a7da89ebf2bff1089e62c794c7272afcde68f5f5ad8983acf688d067c`

```dockerfile
```

-	Layers:
	-	`sha256:c864b878b36d1fbfaac5acc28598ccd96160e7d214da4131228041e666b25d0e`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f4d617789ef531659729800ee7388d1c1f154ba9399fae3bbd757f14b5dcc0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46-debian`

```console
$ docker pull mysql@sha256:9382e4f6f7f013231049ab854de9d0810594d028f4237b67102acc7ade8e3a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.46-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0845b57a4927c2e2e442b0c3c154ebf2bdede7d6e1cb3b5a4b3e8bc1d0e69e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183493846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecd5f2526848a17828c97ea713b778389f599988dc03bb40817bbd0f4e8cff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 22 Apr 2026 01:41:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:42:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:42:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 22 Apr 2026 01:42:07 GMT
ENV MYSQL_VERSION=8.0.46-1debian12
# Wed, 22 Apr 2026 01:42:07 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Apr 2026 01:42:17 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 22 Apr 2026 01:42:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:42:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Apr 2026 01:42:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855a4662f4674f4b2fa5b3319559ce3157688e702d8c2a79583f0da1351e556`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8a7b62f21cd8c4c97cd9f0ac47e47d244e51a06b6c9d503173911a5511e0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.4 MB (4423340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9904ed9c36af76fad8fec577f30214c654ee4d5b049c97f3bf60a035c596e2`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 1.2 MB (1248703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223423e03ce3b1462874ffb00ccf06b7d33ccdfaf4ab8d5267d4b1fcb2a3461`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd0e9a8806dfb4190a5efb53b9068f1473ec79c114ae9acf64e04ae785cfd3`  
		Last Modified: Wed, 22 Apr 2026 01:42:42 GMT  
		Size: 15.3 MB (15295542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56737b600a7ed7a14d1e8410aa58f2c34e1a13828090dbb7dbd4fc8a60dba3d`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c65b70c20a21019513cbc8a61d63aa4f5899645c90ecb9f3d2e2151267969e`  
		Last Modified: Wed, 22 Apr 2026 01:42:41 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2450db828e1da3146b24825caf9ec6f014b7bd17c535dd6aea175bcab19d8`  
		Last Modified: Wed, 22 Apr 2026 01:42:45 GMT  
		Size: 134.3 MB (134279198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f61b0173611c4be67c102358804af4fbd8a1c40b8ac915470077320617e17`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908b55f16b6979dab8bf2917860fefd90e59605fc97bf7c1df4914d6d231c81`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4531d449fbdc31a0aa3f36772fc8c521bfa962e70bab3a5abd4d3a4854ac79`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:c3a78f9613889dbaa4d0174c1b5fb8b5cbeb0582a4879cf79141c74c25fa3e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f692ec2a7da89ebf2bff1089e62c794c7272afcde68f5f5ad8983acf688d067c`

```dockerfile
```

-	Layers:
	-	`sha256:c864b878b36d1fbfaac5acc28598ccd96160e7d214da4131228041e666b25d0e`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f4d617789ef531659729800ee7388d1c1f154ba9399fae3bbd757f14b5dcc0`  
		Last Modified: Wed, 22 Apr 2026 01:42:40 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46-oracle`

```console
$ docker pull mysql@sha256:7dcddc01f13bab2f15cde676d44d01f61fc9f99fe7785e86196dfc07d358ae2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.46-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:62fb722c78b24245ddff1796a0fcee4a49cc5b87e0aaaf20c92d1da9e0a2497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233581538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd09145362dfe6831b14545de3d5fd6cc75c37cfd6ef8561429c1fc73518b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:59:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:59:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:59:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 23:00:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:01:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 23:01:20 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 23:01:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 23:01:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 23:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 23:01:20 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 23:01:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6c7b50a938e4f81a40ed970b0a1b4d6409d55032d50c0d8a30042b484226f`  
		Last Modified: Mon, 04 May 2026 23:01:51 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5d1ac74c19e81a17008c972f1ca25e9c4dc509307c3eee1382e7301f0f7a4`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 783.6 KB (783558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74d296605b0eb8f94dd83441a08a413f4ae4f2aafa9e7d1e2da5adcdade645`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 6.2 MB (6173009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297d04cfe4705c95a7d1a6abb5831e3637edfebdb6b639661c8c66ff2220cd64`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a3e0d4e4b216b443a3125ae3f947d8d0e9df399ba4af9bbb5823703c95c1f`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63160a5eda1f2bc97de740813d14908519eba5d1d59da5f7f6934126d33ce17`  
		Last Modified: Mon, 04 May 2026 23:01:55 GMT  
		Size: 49.9 MB (49934187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7534d1db9f8dcc7acdd28f0655c93bd0b045dee128866ff2809c833a6462eaf1`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ec2dab01d93d549839d59c815b48a834beca654fc9d45a86eaddc8fd82cc5a`  
		Last Modified: Mon, 04 May 2026 23:01:57 GMT  
		Size: 129.4 MB (129371339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab24264a27e9ec0085b30b83b81272417504c9e231d006975e9956af3526a3ab`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d30d9fbee877d823d9807f43df6c030983d61d7a645d0f5ac2c7154a8abd12`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fed8ae184a51c4b7d9cc23dd38a0a1bed605380eb6f11e0f45dd08c2db084d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27122045730314b10f63d94f0d07039b28a4aa531f13ae4b0563f16e3a397235`

```dockerfile
```

-	Layers:
	-	`sha256:af166387641d84cdf7a5b00f7127dcdd3f9829c942fc697d6275e92b331abe0f`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 15.4 MB (15434095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796812c73292ea535203de666541c84fa0203f9ad3a960045dfbb1a55c8cf062`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.46-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:213bbfaf699693a40a20a12bb4342d2589a15a3dc7153db698eaed252a92458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229139579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e118f56c5963e079252e0d6e2978c9c010eb7fc7aaaec100e367796b5dd08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:09:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:11:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:11:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:11:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:11:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:11:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a53223cb4cb4f2abbb070ad06dba8b1c95c6deac4666e954d223c97ad0b471`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f24d93d521ecd5f1ede50bb6157f3b19c601ddc22d307b2880b6dddbe03b2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c0b299cb470fda07120beb3b619b655387ec5f4a2da72ce9330d2f194c7029`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 5.8 MB (5790720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce425b17caf10ed18a4d56a89d8a1c078c9fe1c7d3edd22fc45f3c0bd913da2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b2852d2a9df74e94222dd4d151b25ba5397968a479cc85cc31b23041f871a0`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605b7f42ac6ece809a06d59a07fa37ebc3ba9373b1aa1a22966677931451e41a`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 48.8 MB (48787669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1959e4a06a1cc7ddadccce363a91f5bd01ae4f93be2cdbf461f87f2e8529ac81`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa30ab141b5a5b854dbb1adf9111599d6d2b71c8819a1bb1fae8ccd5ee0f7c2c`  
		Last Modified: Mon, 04 May 2026 21:11:49 GMT  
		Size: 127.9 MB (127915155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42505e6e6b9177d92b219bcdfda82f6718e3de57a8bd37ff12c40ccf53db37d8`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcb28d1dfcf6af3f3b0b4cffdb6807ddbb75d4e91ecdae2c33728f0a27214f3`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9b41c768826231fff8ecb98e1f440b5c1d424c969657458da2b82e85437ec0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0adef218acadd6ab1e34ab53c0140485524c67d6ae8c87f54aa9c14592c3c`

```dockerfile
```

-	Layers:
	-	`sha256:578f543767f02fd88515a88c5d349ea41c6520d836c4ceaf95626a610a89e3ed`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 15.4 MB (15432443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0e30178db86f71b9c37b48b46e426909127768c1fd481ccb7e74423480b9ce`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.46-oraclelinux9`

```console
$ docker pull mysql@sha256:7dcddc01f13bab2f15cde676d44d01f61fc9f99fe7785e86196dfc07d358ae2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.46-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:62fb722c78b24245ddff1796a0fcee4a49cc5b87e0aaaf20c92d1da9e0a2497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233581538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd09145362dfe6831b14545de3d5fd6cc75c37cfd6ef8561429c1fc73518b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 22:04:15 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:04:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:59:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 22:59:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 22:59:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 23:00:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 23:00:13 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:00:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 23:00:43 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 23:00:43 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 23:01:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 23:01:20 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 23:01:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 23:01:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 23:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 23:01:20 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 23:01:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:edf85873f64e24f7d5f7e8a2fc498afd54aa646dbf1bc7d5a2f1bf03b096d973`  
		Last Modified: Mon, 04 May 2026 22:04:27 GMT  
		Size: 47.3 MB (47309856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6c7b50a938e4f81a40ed970b0a1b4d6409d55032d50c0d8a30042b484226f`  
		Last Modified: Mon, 04 May 2026 23:01:51 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5d1ac74c19e81a17008c972f1ca25e9c4dc509307c3eee1382e7301f0f7a4`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 783.6 KB (783558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74d296605b0eb8f94dd83441a08a413f4ae4f2aafa9e7d1e2da5adcdade645`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 6.2 MB (6173009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297d04cfe4705c95a7d1a6abb5831e3637edfebdb6b639661c8c66ff2220cd64`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a3e0d4e4b216b443a3125ae3f947d8d0e9df399ba4af9bbb5823703c95c1f`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63160a5eda1f2bc97de740813d14908519eba5d1d59da5f7f6934126d33ce17`  
		Last Modified: Mon, 04 May 2026 23:01:55 GMT  
		Size: 49.9 MB (49934187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7534d1db9f8dcc7acdd28f0655c93bd0b045dee128866ff2809c833a6462eaf1`  
		Last Modified: Mon, 04 May 2026 23:01:53 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ec2dab01d93d549839d59c815b48a834beca654fc9d45a86eaddc8fd82cc5a`  
		Last Modified: Mon, 04 May 2026 23:01:57 GMT  
		Size: 129.4 MB (129371339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab24264a27e9ec0085b30b83b81272417504c9e231d006975e9956af3526a3ab`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d30d9fbee877d823d9807f43df6c030983d61d7a645d0f5ac2c7154a8abd12`  
		Last Modified: Mon, 04 May 2026 23:01:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fed8ae184a51c4b7d9cc23dd38a0a1bed605380eb6f11e0f45dd08c2db084d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27122045730314b10f63d94f0d07039b28a4aa531f13ae4b0563f16e3a397235`

```dockerfile
```

-	Layers:
	-	`sha256:af166387641d84cdf7a5b00f7127dcdd3f9829c942fc697d6275e92b331abe0f`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 15.4 MB (15434095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796812c73292ea535203de666541c84fa0203f9ad3a960045dfbb1a55c8cf062`  
		Last Modified: Mon, 04 May 2026 23:01:52 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.46-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:213bbfaf699693a40a20a12bb4342d2589a15a3dc7153db698eaed252a92458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229139579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e118f56c5963e079252e0d6e2978c9c010eb7fc7aaaec100e367796b5dd08f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 04 May 2026 21:01:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:09:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 04 May 2026 21:09:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 04 May 2026 21:09:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 04 May 2026 21:09:52 GMT
ENV MYSQL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:09:52 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 04 May 2026 21:10:28 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 04 May 2026 21:10:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.46-1.el9
# Mon, 04 May 2026 21:11:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 04 May 2026 21:11:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 May 2026 21:11:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 May 2026 21:11:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 04 May 2026 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 May 2026 21:11:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 04 May 2026 21:11:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ad770837e7894e962af6cad8abb6dc5110f2ed3e8eb4644fc3af5abf8449fcc1`  
		Last Modified: Mon, 04 May 2026 21:02:08 GMT  
		Size: 45.9 MB (45898922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a53223cb4cb4f2abbb070ad06dba8b1c95c6deac4666e954d223c97ad0b471`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f24d93d521ecd5f1ede50bb6157f3b19c601ddc22d307b2880b6dddbe03b2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c0b299cb470fda07120beb3b619b655387ec5f4a2da72ce9330d2f194c7029`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 5.8 MB (5790720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce425b17caf10ed18a4d56a89d8a1c078c9fe1c7d3edd22fc45f3c0bd913da2`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b2852d2a9df74e94222dd4d151b25ba5397968a479cc85cc31b23041f871a0`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605b7f42ac6ece809a06d59a07fa37ebc3ba9373b1aa1a22966677931451e41a`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 48.8 MB (48787669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1959e4a06a1cc7ddadccce363a91f5bd01ae4f93be2cdbf461f87f2e8529ac81`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa30ab141b5a5b854dbb1adf9111599d6d2b71c8819a1bb1fae8ccd5ee0f7c2c`  
		Last Modified: Mon, 04 May 2026 21:11:49 GMT  
		Size: 127.9 MB (127915155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42505e6e6b9177d92b219bcdfda82f6718e3de57a8bd37ff12c40ccf53db37d8`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcb28d1dfcf6af3f3b0b4cffdb6807ddbb75d4e91ecdae2c33728f0a27214f3`  
		Last Modified: Mon, 04 May 2026 21:11:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.46-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9b41c768826231fff8ecb98e1f440b5c1d424c969657458da2b82e85437ec0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15467602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0adef218acadd6ab1e34ab53c0140485524c67d6ae8c87f54aa9c14592c3c`

```dockerfile
```

-	Layers:
	-	`sha256:578f543767f02fd88515a88c5d349ea41c6520d836c4ceaf95626a610a89e3ed`  
		Last Modified: Mon, 04 May 2026 21:11:45 GMT  
		Size: 15.4 MB (15432443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0e30178db86f71b9c37b48b46e426909127768c1fd481ccb7e74423480b9ce`  
		Last Modified: Mon, 04 May 2026 21:11:44 GMT  
		Size: 35.2 KB (35159 bytes)  
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
