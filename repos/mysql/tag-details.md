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
-	[`mysql:8.0.43`](#mysql8043)
-	[`mysql:8.0.43-bookworm`](#mysql8043-bookworm)
-	[`mysql:8.0.43-debian`](#mysql8043-debian)
-	[`mysql:8.0.43-oracle`](#mysql8043-oracle)
-	[`mysql:8.0.43-oraclelinux9`](#mysql8043-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.6`](#mysql846)
-	[`mysql:8.4.6-oracle`](#mysql846-oracle)
-	[`mysql:8.4.6-oraclelinux9`](#mysql846-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.4`](#mysql94)
-	[`mysql:9.4-oracle`](#mysql94-oracle)
-	[`mysql:9.4-oraclelinux9`](#mysql94-oraclelinux9)
-	[`mysql:9.4.0`](#mysql940)
-	[`mysql:9.4.0-oracle`](#mysql940-oracle)
-	[`mysql:9.4.0-oraclelinux9`](#mysql940-oraclelinux9)
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
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:9ece5be897e6b58c5756f2f4378bcc2deab42cda5bf363891d141c21b5c6e0de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:0df1fa02875e2b873640f068d6cf1ebf9982bded82821465721a503a6e898167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235834455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19538dd7d235eca1d38163bdb4124d5b52a7bcae4ed20c8dd35af64dbd1434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48934deb977008d432d432c942d0c9bf0311e82df69fe878ec98ca432c1275b1`  
		Last Modified: Mon, 08 Sep 2025 22:42:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021b6107b9d0ca5c81a80c275a93fe4a4228d99b7750cc1b8cf22f9041aa2bf2`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16089ebc58ba2085049e3e3e723eb2ed964e8372a9e7854f1a15e680e951`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 6.8 MB (6818663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dcaa70f774ccc9d181d68028676501176ea8e2b3a9e91962ef3bcec1b241d`  
		Last Modified: Mon, 08 Sep 2025 22:42:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a465986d66649506815977bfabe50e4a523971b55edcb36af6211c43f6b609`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa9cc59961edad552866ec7077aa4eefe8dab0dac63791e21ec3cdf0213b6c`  
		Last Modified: Mon, 08 Sep 2025 23:10:08 GMT  
		Size: 49.8 MB (49820062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a27c0ce790fb7bc36776b79407e200eface044a5f5d998e99a99825eef13b97`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390885da77e47ae7ff7bccf3a96b161f38fa9233924d22f92361fce8f13c4079`  
		Last Modified: Mon, 08 Sep 2025 23:09:57 GMT  
		Size: 128.9 MB (128906779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2ca504238ac4a3ac80c3025c09e9e1593957b6b61940b5e58193ee7108faa`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f78235dcb83bdab237d2a5f844020e6ad96e215a36446e3d55bf3a7b10fb65`  
		Last Modified: Mon, 08 Sep 2025 22:43:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:bf60ab88436e18691018311be97b29716697da2207fb521e75ef173b8a14f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a573e945f24923ac1241b29ba35ffd6096bc1d60ece181aad5040261e4ef738`

```dockerfile
```

-	Layers:
	-	`sha256:30b6bb4730c967c52f1a703b7ec74602ef6a05d7b1a6673951216b7fbcb91a94`  
		Last Modified: Tue, 09 Sep 2025 00:02:39 GMT  
		Size: 14.5 MB (14528097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c9c8cdcc30e658612165ca5a31cd99fe60d368f07f0084473c887ab18ce37`  
		Last Modified: Tue, 09 Sep 2025 00:02:40 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:44f3046fa0eac90420310151e9959959131c79c7ba7bc670edb7dc1d56cc6d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231621215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5899f96253cec7897b1c32ddcc6f57a4c8fb47bb01d53bf18d2781b3d2dce7a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dfcacb56a5a54ef850255b73ddade5a2fcf52683258ff8f63f58cc435efbbe`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b1f39ad9c5b4a7a28de7069c0b1daa1500ad40bbf0d45dd125518804b45ba`  
		Last Modified: Thu, 21 Aug 2025 21:44:55 GMT  
		Size: 48.7 MB (48677572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e196ab7d9d74832d6a80a475e2af06b5e03e0674a96aac072554941cfe3e6c`  
		Last Modified: Thu, 21 Aug 2025 21:07:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13524f5997c14a8814389dee474a59b93e5e5553bf9596bbadc7fe4b9f166ae5`  
		Last Modified: Thu, 21 Aug 2025 21:45:01 GMT  
		Size: 127.5 MB (127488080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16d0631edced14a95b1b607975b71ae1d4f66b8ae11f09c4a9ba358595f1229`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ebbefeaf6c1ca7184f4be10ba1569ea222109d3b6e7f94655b4445ce79a1f4`  
		Last Modified: Thu, 21 Aug 2025 21:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:6a81f0012ce016623881070350b9f066ca32c0e717f9d8e6000b62de70452be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ef213789260261eb5b71e3ecc0fb45195b08fcf9298813ac1d740d487e15f1`

```dockerfile
```

-	Layers:
	-	`sha256:0d99250dea0f345c688c802f39338a140b92b19e81ec25ccba59c476881e8c0f`  
		Last Modified: Fri, 22 Aug 2025 00:02:36 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91500571b6a34d8b3ab75a92732cfe47b9c3317e23d5f4300be662c3bdd7e03`  
		Last Modified: Fri, 22 Aug 2025 00:02:38 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:115a6e05ed2e9e2acb8c80902d482e6b028c613a48f31de691d9d9b32a826957
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:39b35539215cc62684d39f072105ac8936371424846df38c7599fcc79d0c68ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183367059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0047b48c4f5a176322e0b04fc9b44a181b9efc56845dd16b5b373654345f9930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 20:09:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Mon, 08 Sep 2025 20:09:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f32ffcc4d4a775909383bcd8d2e269500c600abdeec094ac96f9d893962431`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b321a618139936dc78076d50d410d2c04752ec44ec03a8f2fc030f106625bcaf`  
		Last Modified: Tue, 09 Sep 2025 00:02:57 GMT  
		Size: 4.4 MB (4422989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c841bc79f64f2631f71f3e89d73f1e9db4d295c0fc237ec8168709ba64e8bc`  
		Last Modified: Mon, 08 Sep 2025 23:22:13 GMT  
		Size: 1.2 MB (1247514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306c1742de9df3d11725b4ceaa15bea9298f2c51443e7477f012f41d8e2162d`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18072a596e5bede43c6045ea8862f635c47b8c92493bcc71c11a2aa139507814`  
		Last Modified: Tue, 09 Sep 2025 00:02:59 GMT  
		Size: 15.3 MB (15294623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5661af208872c939bba00e210e71c39791197c4c230bb54c516b9f8cee2ac108`  
		Last Modified: Mon, 08 Sep 2025 23:22:11 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836dd6c53a4954030dd6f36b6a50a67e28d1830471a178ebe0e318701f69031f`  
		Last Modified: Mon, 08 Sep 2025 23:22:11 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8adddcee34e3e4fba2487e3471ea01db3015057c012cefc6bfd13f3e58fcfd`  
		Last Modified: Tue, 09 Sep 2025 00:03:07 GMT  
		Size: 134.2 MB (134163320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd3e72e94e86bf9498560c43af57090aa373222c5c49452c5dfea9e4376cad`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e41d14bbc0d7c5f366f0505bffea36dcc07b0a7e051e5757f3bfab8bfa02e4`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff05668ee8f63f723940795085d559d8dbc223e33475381b9002864f68ff58b`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:d21280d6c72dc2f74d1f6825b4a69bc54f682530fddd54fd562bba8fb3df3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fcb1f04ab003cf2d0dd6a773ff9950670e8884a710f0e071ba0aeed61ab192`

```dockerfile
```

-	Layers:
	-	`sha256:a89ff63ac0bcc4bc2847cfcfa43610cde7b3fa690d3a54f43c2e258e0a8b224a`  
		Last Modified: Tue, 09 Sep 2025 00:02:45 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80812ef99860add889decf87e67f6b742a5a5cf7d168fa554bbf1c7a0be49857`  
		Last Modified: Tue, 09 Sep 2025 00:02:45 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:115a6e05ed2e9e2acb8c80902d482e6b028c613a48f31de691d9d9b32a826957
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:39b35539215cc62684d39f072105ac8936371424846df38c7599fcc79d0c68ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183367059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0047b48c4f5a176322e0b04fc9b44a181b9efc56845dd16b5b373654345f9930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 20:09:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Mon, 08 Sep 2025 20:09:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f32ffcc4d4a775909383bcd8d2e269500c600abdeec094ac96f9d893962431`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b321a618139936dc78076d50d410d2c04752ec44ec03a8f2fc030f106625bcaf`  
		Last Modified: Tue, 09 Sep 2025 00:02:57 GMT  
		Size: 4.4 MB (4422989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c841bc79f64f2631f71f3e89d73f1e9db4d295c0fc237ec8168709ba64e8bc`  
		Last Modified: Mon, 08 Sep 2025 23:22:13 GMT  
		Size: 1.2 MB (1247514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306c1742de9df3d11725b4ceaa15bea9298f2c51443e7477f012f41d8e2162d`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18072a596e5bede43c6045ea8862f635c47b8c92493bcc71c11a2aa139507814`  
		Last Modified: Tue, 09 Sep 2025 00:02:59 GMT  
		Size: 15.3 MB (15294623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5661af208872c939bba00e210e71c39791197c4c230bb54c516b9f8cee2ac108`  
		Last Modified: Mon, 08 Sep 2025 23:22:11 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836dd6c53a4954030dd6f36b6a50a67e28d1830471a178ebe0e318701f69031f`  
		Last Modified: Mon, 08 Sep 2025 23:22:11 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8adddcee34e3e4fba2487e3471ea01db3015057c012cefc6bfd13f3e58fcfd`  
		Last Modified: Tue, 09 Sep 2025 00:03:07 GMT  
		Size: 134.2 MB (134163320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd3e72e94e86bf9498560c43af57090aa373222c5c49452c5dfea9e4376cad`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e41d14bbc0d7c5f366f0505bffea36dcc07b0a7e051e5757f3bfab8bfa02e4`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff05668ee8f63f723940795085d559d8dbc223e33475381b9002864f68ff58b`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:d21280d6c72dc2f74d1f6825b4a69bc54f682530fddd54fd562bba8fb3df3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fcb1f04ab003cf2d0dd6a773ff9950670e8884a710f0e071ba0aeed61ab192`

```dockerfile
```

-	Layers:
	-	`sha256:a89ff63ac0bcc4bc2847cfcfa43610cde7b3fa690d3a54f43c2e258e0a8b224a`  
		Last Modified: Tue, 09 Sep 2025 00:02:45 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80812ef99860add889decf87e67f6b742a5a5cf7d168fa554bbf1c7a0be49857`  
		Last Modified: Tue, 09 Sep 2025 00:02:45 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:9ece5be897e6b58c5756f2f4378bcc2deab42cda5bf363891d141c21b5c6e0de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0df1fa02875e2b873640f068d6cf1ebf9982bded82821465721a503a6e898167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235834455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19538dd7d235eca1d38163bdb4124d5b52a7bcae4ed20c8dd35af64dbd1434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48934deb977008d432d432c942d0c9bf0311e82df69fe878ec98ca432c1275b1`  
		Last Modified: Mon, 08 Sep 2025 22:42:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021b6107b9d0ca5c81a80c275a93fe4a4228d99b7750cc1b8cf22f9041aa2bf2`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16089ebc58ba2085049e3e3e723eb2ed964e8372a9e7854f1a15e680e951`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 6.8 MB (6818663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dcaa70f774ccc9d181d68028676501176ea8e2b3a9e91962ef3bcec1b241d`  
		Last Modified: Mon, 08 Sep 2025 22:42:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a465986d66649506815977bfabe50e4a523971b55edcb36af6211c43f6b609`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa9cc59961edad552866ec7077aa4eefe8dab0dac63791e21ec3cdf0213b6c`  
		Last Modified: Mon, 08 Sep 2025 23:10:08 GMT  
		Size: 49.8 MB (49820062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a27c0ce790fb7bc36776b79407e200eface044a5f5d998e99a99825eef13b97`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390885da77e47ae7ff7bccf3a96b161f38fa9233924d22f92361fce8f13c4079`  
		Last Modified: Mon, 08 Sep 2025 23:09:57 GMT  
		Size: 128.9 MB (128906779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2ca504238ac4a3ac80c3025c09e9e1593957b6b61940b5e58193ee7108faa`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f78235dcb83bdab237d2a5f844020e6ad96e215a36446e3d55bf3a7b10fb65`  
		Last Modified: Mon, 08 Sep 2025 22:43:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bf60ab88436e18691018311be97b29716697da2207fb521e75ef173b8a14f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a573e945f24923ac1241b29ba35ffd6096bc1d60ece181aad5040261e4ef738`

```dockerfile
```

-	Layers:
	-	`sha256:30b6bb4730c967c52f1a703b7ec74602ef6a05d7b1a6673951216b7fbcb91a94`  
		Last Modified: Tue, 09 Sep 2025 00:02:39 GMT  
		Size: 14.5 MB (14528097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c9c8cdcc30e658612165ca5a31cd99fe60d368f07f0084473c887ab18ce37`  
		Last Modified: Tue, 09 Sep 2025 00:02:40 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:44f3046fa0eac90420310151e9959959131c79c7ba7bc670edb7dc1d56cc6d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231621215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5899f96253cec7897b1c32ddcc6f57a4c8fb47bb01d53bf18d2781b3d2dce7a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dfcacb56a5a54ef850255b73ddade5a2fcf52683258ff8f63f58cc435efbbe`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b1f39ad9c5b4a7a28de7069c0b1daa1500ad40bbf0d45dd125518804b45ba`  
		Last Modified: Thu, 21 Aug 2025 21:44:55 GMT  
		Size: 48.7 MB (48677572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e196ab7d9d74832d6a80a475e2af06b5e03e0674a96aac072554941cfe3e6c`  
		Last Modified: Thu, 21 Aug 2025 21:07:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13524f5997c14a8814389dee474a59b93e5e5553bf9596bbadc7fe4b9f166ae5`  
		Last Modified: Thu, 21 Aug 2025 21:45:01 GMT  
		Size: 127.5 MB (127488080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16d0631edced14a95b1b607975b71ae1d4f66b8ae11f09c4a9ba358595f1229`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ebbefeaf6c1ca7184f4be10ba1569ea222109d3b6e7f94655b4445ce79a1f4`  
		Last Modified: Thu, 21 Aug 2025 21:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a81f0012ce016623881070350b9f066ca32c0e717f9d8e6000b62de70452be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ef213789260261eb5b71e3ecc0fb45195b08fcf9298813ac1d740d487e15f1`

```dockerfile
```

-	Layers:
	-	`sha256:0d99250dea0f345c688c802f39338a140b92b19e81ec25ccba59c476881e8c0f`  
		Last Modified: Fri, 22 Aug 2025 00:02:36 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91500571b6a34d8b3ab75a92732cfe47b9c3317e23d5f4300be662c3bdd7e03`  
		Last Modified: Fri, 22 Aug 2025 00:02:38 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:9ece5be897e6b58c5756f2f4378bcc2deab42cda5bf363891d141c21b5c6e0de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0df1fa02875e2b873640f068d6cf1ebf9982bded82821465721a503a6e898167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235834455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19538dd7d235eca1d38163bdb4124d5b52a7bcae4ed20c8dd35af64dbd1434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48934deb977008d432d432c942d0c9bf0311e82df69fe878ec98ca432c1275b1`  
		Last Modified: Mon, 08 Sep 2025 22:42:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021b6107b9d0ca5c81a80c275a93fe4a4228d99b7750cc1b8cf22f9041aa2bf2`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16089ebc58ba2085049e3e3e723eb2ed964e8372a9e7854f1a15e680e951`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 6.8 MB (6818663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dcaa70f774ccc9d181d68028676501176ea8e2b3a9e91962ef3bcec1b241d`  
		Last Modified: Mon, 08 Sep 2025 22:42:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a465986d66649506815977bfabe50e4a523971b55edcb36af6211c43f6b609`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa9cc59961edad552866ec7077aa4eefe8dab0dac63791e21ec3cdf0213b6c`  
		Last Modified: Mon, 08 Sep 2025 23:10:08 GMT  
		Size: 49.8 MB (49820062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a27c0ce790fb7bc36776b79407e200eface044a5f5d998e99a99825eef13b97`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390885da77e47ae7ff7bccf3a96b161f38fa9233924d22f92361fce8f13c4079`  
		Last Modified: Mon, 08 Sep 2025 23:09:57 GMT  
		Size: 128.9 MB (128906779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2ca504238ac4a3ac80c3025c09e9e1593957b6b61940b5e58193ee7108faa`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f78235dcb83bdab237d2a5f844020e6ad96e215a36446e3d55bf3a7b10fb65`  
		Last Modified: Mon, 08 Sep 2025 22:43:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bf60ab88436e18691018311be97b29716697da2207fb521e75ef173b8a14f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a573e945f24923ac1241b29ba35ffd6096bc1d60ece181aad5040261e4ef738`

```dockerfile
```

-	Layers:
	-	`sha256:30b6bb4730c967c52f1a703b7ec74602ef6a05d7b1a6673951216b7fbcb91a94`  
		Last Modified: Tue, 09 Sep 2025 00:02:39 GMT  
		Size: 14.5 MB (14528097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c9c8cdcc30e658612165ca5a31cd99fe60d368f07f0084473c887ab18ce37`  
		Last Modified: Tue, 09 Sep 2025 00:02:40 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:44f3046fa0eac90420310151e9959959131c79c7ba7bc670edb7dc1d56cc6d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231621215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5899f96253cec7897b1c32ddcc6f57a4c8fb47bb01d53bf18d2781b3d2dce7a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dfcacb56a5a54ef850255b73ddade5a2fcf52683258ff8f63f58cc435efbbe`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b1f39ad9c5b4a7a28de7069c0b1daa1500ad40bbf0d45dd125518804b45ba`  
		Last Modified: Thu, 21 Aug 2025 21:44:55 GMT  
		Size: 48.7 MB (48677572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e196ab7d9d74832d6a80a475e2af06b5e03e0674a96aac072554941cfe3e6c`  
		Last Modified: Thu, 21 Aug 2025 21:07:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13524f5997c14a8814389dee474a59b93e5e5553bf9596bbadc7fe4b9f166ae5`  
		Last Modified: Thu, 21 Aug 2025 21:45:01 GMT  
		Size: 127.5 MB (127488080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16d0631edced14a95b1b607975b71ae1d4f66b8ae11f09c4a9ba358595f1229`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ebbefeaf6c1ca7184f4be10ba1569ea222109d3b6e7f94655b4445ce79a1f4`  
		Last Modified: Thu, 21 Aug 2025 21:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a81f0012ce016623881070350b9f066ca32c0e717f9d8e6000b62de70452be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ef213789260261eb5b71e3ecc0fb45195b08fcf9298813ac1d740d487e15f1`

```dockerfile
```

-	Layers:
	-	`sha256:0d99250dea0f345c688c802f39338a140b92b19e81ec25ccba59c476881e8c0f`  
		Last Modified: Fri, 22 Aug 2025 00:02:36 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91500571b6a34d8b3ab75a92732cfe47b9c3317e23d5f4300be662c3bdd7e03`  
		Last Modified: Fri, 22 Aug 2025 00:02:38 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43`

```console
$ docker pull mysql@sha256:9ece5be897e6b58c5756f2f4378bcc2deab42cda5bf363891d141c21b5c6e0de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43` - linux; amd64

```console
$ docker pull mysql@sha256:0df1fa02875e2b873640f068d6cf1ebf9982bded82821465721a503a6e898167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235834455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19538dd7d235eca1d38163bdb4124d5b52a7bcae4ed20c8dd35af64dbd1434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48934deb977008d432d432c942d0c9bf0311e82df69fe878ec98ca432c1275b1`  
		Last Modified: Mon, 08 Sep 2025 22:42:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021b6107b9d0ca5c81a80c275a93fe4a4228d99b7750cc1b8cf22f9041aa2bf2`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16089ebc58ba2085049e3e3e723eb2ed964e8372a9e7854f1a15e680e951`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 6.8 MB (6818663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dcaa70f774ccc9d181d68028676501176ea8e2b3a9e91962ef3bcec1b241d`  
		Last Modified: Mon, 08 Sep 2025 22:42:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a465986d66649506815977bfabe50e4a523971b55edcb36af6211c43f6b609`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa9cc59961edad552866ec7077aa4eefe8dab0dac63791e21ec3cdf0213b6c`  
		Last Modified: Mon, 08 Sep 2025 23:10:08 GMT  
		Size: 49.8 MB (49820062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a27c0ce790fb7bc36776b79407e200eface044a5f5d998e99a99825eef13b97`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390885da77e47ae7ff7bccf3a96b161f38fa9233924d22f92361fce8f13c4079`  
		Last Modified: Mon, 08 Sep 2025 23:09:57 GMT  
		Size: 128.9 MB (128906779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2ca504238ac4a3ac80c3025c09e9e1593957b6b61940b5e58193ee7108faa`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f78235dcb83bdab237d2a5f844020e6ad96e215a36446e3d55bf3a7b10fb65`  
		Last Modified: Mon, 08 Sep 2025 22:43:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:bf60ab88436e18691018311be97b29716697da2207fb521e75ef173b8a14f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a573e945f24923ac1241b29ba35ffd6096bc1d60ece181aad5040261e4ef738`

```dockerfile
```

-	Layers:
	-	`sha256:30b6bb4730c967c52f1a703b7ec74602ef6a05d7b1a6673951216b7fbcb91a94`  
		Last Modified: Tue, 09 Sep 2025 00:02:39 GMT  
		Size: 14.5 MB (14528097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c9c8cdcc30e658612165ca5a31cd99fe60d368f07f0084473c887ab18ce37`  
		Last Modified: Tue, 09 Sep 2025 00:02:40 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:44f3046fa0eac90420310151e9959959131c79c7ba7bc670edb7dc1d56cc6d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231621215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5899f96253cec7897b1c32ddcc6f57a4c8fb47bb01d53bf18d2781b3d2dce7a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dfcacb56a5a54ef850255b73ddade5a2fcf52683258ff8f63f58cc435efbbe`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b1f39ad9c5b4a7a28de7069c0b1daa1500ad40bbf0d45dd125518804b45ba`  
		Last Modified: Thu, 21 Aug 2025 21:44:55 GMT  
		Size: 48.7 MB (48677572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e196ab7d9d74832d6a80a475e2af06b5e03e0674a96aac072554941cfe3e6c`  
		Last Modified: Thu, 21 Aug 2025 21:07:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13524f5997c14a8814389dee474a59b93e5e5553bf9596bbadc7fe4b9f166ae5`  
		Last Modified: Thu, 21 Aug 2025 21:45:01 GMT  
		Size: 127.5 MB (127488080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16d0631edced14a95b1b607975b71ae1d4f66b8ae11f09c4a9ba358595f1229`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ebbefeaf6c1ca7184f4be10ba1569ea222109d3b6e7f94655b4445ce79a1f4`  
		Last Modified: Thu, 21 Aug 2025 21:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:6a81f0012ce016623881070350b9f066ca32c0e717f9d8e6000b62de70452be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ef213789260261eb5b71e3ecc0fb45195b08fcf9298813ac1d740d487e15f1`

```dockerfile
```

-	Layers:
	-	`sha256:0d99250dea0f345c688c802f39338a140b92b19e81ec25ccba59c476881e8c0f`  
		Last Modified: Fri, 22 Aug 2025 00:02:36 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91500571b6a34d8b3ab75a92732cfe47b9c3317e23d5f4300be662c3bdd7e03`  
		Last Modified: Fri, 22 Aug 2025 00:02:38 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-bookworm`

```console
$ docker pull mysql@sha256:115a6e05ed2e9e2acb8c80902d482e6b028c613a48f31de691d9d9b32a826957
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.43-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:39b35539215cc62684d39f072105ac8936371424846df38c7599fcc79d0c68ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183367059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0047b48c4f5a176322e0b04fc9b44a181b9efc56845dd16b5b373654345f9930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 20:09:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Mon, 08 Sep 2025 20:09:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f32ffcc4d4a775909383bcd8d2e269500c600abdeec094ac96f9d893962431`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b321a618139936dc78076d50d410d2c04752ec44ec03a8f2fc030f106625bcaf`  
		Last Modified: Tue, 09 Sep 2025 00:02:57 GMT  
		Size: 4.4 MB (4422989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c841bc79f64f2631f71f3e89d73f1e9db4d295c0fc237ec8168709ba64e8bc`  
		Last Modified: Mon, 08 Sep 2025 23:22:13 GMT  
		Size: 1.2 MB (1247514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306c1742de9df3d11725b4ceaa15bea9298f2c51443e7477f012f41d8e2162d`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18072a596e5bede43c6045ea8862f635c47b8c92493bcc71c11a2aa139507814`  
		Last Modified: Tue, 09 Sep 2025 00:02:59 GMT  
		Size: 15.3 MB (15294623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5661af208872c939bba00e210e71c39791197c4c230bb54c516b9f8cee2ac108`  
		Last Modified: Mon, 08 Sep 2025 23:22:11 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836dd6c53a4954030dd6f36b6a50a67e28d1830471a178ebe0e318701f69031f`  
		Last Modified: Mon, 08 Sep 2025 23:22:11 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8adddcee34e3e4fba2487e3471ea01db3015057c012cefc6bfd13f3e58fcfd`  
		Last Modified: Tue, 09 Sep 2025 00:03:07 GMT  
		Size: 134.2 MB (134163320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd3e72e94e86bf9498560c43af57090aa373222c5c49452c5dfea9e4376cad`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e41d14bbc0d7c5f366f0505bffea36dcc07b0a7e051e5757f3bfab8bfa02e4`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff05668ee8f63f723940795085d559d8dbc223e33475381b9002864f68ff58b`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:d21280d6c72dc2f74d1f6825b4a69bc54f682530fddd54fd562bba8fb3df3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fcb1f04ab003cf2d0dd6a773ff9950670e8884a710f0e071ba0aeed61ab192`

```dockerfile
```

-	Layers:
	-	`sha256:a89ff63ac0bcc4bc2847cfcfa43610cde7b3fa690d3a54f43c2e258e0a8b224a`  
		Last Modified: Tue, 09 Sep 2025 00:02:45 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80812ef99860add889decf87e67f6b742a5a5cf7d168fa554bbf1c7a0be49857`  
		Last Modified: Tue, 09 Sep 2025 00:02:45 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-debian`

```console
$ docker pull mysql@sha256:115a6e05ed2e9e2acb8c80902d482e6b028c613a48f31de691d9d9b32a826957
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.43-debian` - linux; amd64

```console
$ docker pull mysql@sha256:39b35539215cc62684d39f072105ac8936371424846df38c7599fcc79d0c68ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183367059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0047b48c4f5a176322e0b04fc9b44a181b9efc56845dd16b5b373654345f9930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 08 Sep 2025 20:09:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1debian12
# Mon, 08 Sep 2025 20:09:09 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f32ffcc4d4a775909383bcd8d2e269500c600abdeec094ac96f9d893962431`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b321a618139936dc78076d50d410d2c04752ec44ec03a8f2fc030f106625bcaf`  
		Last Modified: Tue, 09 Sep 2025 00:02:57 GMT  
		Size: 4.4 MB (4422989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c841bc79f64f2631f71f3e89d73f1e9db4d295c0fc237ec8168709ba64e8bc`  
		Last Modified: Mon, 08 Sep 2025 23:22:13 GMT  
		Size: 1.2 MB (1247514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306c1742de9df3d11725b4ceaa15bea9298f2c51443e7477f012f41d8e2162d`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18072a596e5bede43c6045ea8862f635c47b8c92493bcc71c11a2aa139507814`  
		Last Modified: Tue, 09 Sep 2025 00:02:59 GMT  
		Size: 15.3 MB (15294623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5661af208872c939bba00e210e71c39791197c4c230bb54c516b9f8cee2ac108`  
		Last Modified: Mon, 08 Sep 2025 23:22:11 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836dd6c53a4954030dd6f36b6a50a67e28d1830471a178ebe0e318701f69031f`  
		Last Modified: Mon, 08 Sep 2025 23:22:11 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8adddcee34e3e4fba2487e3471ea01db3015057c012cefc6bfd13f3e58fcfd`  
		Last Modified: Tue, 09 Sep 2025 00:03:07 GMT  
		Size: 134.2 MB (134163320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd3e72e94e86bf9498560c43af57090aa373222c5c49452c5dfea9e4376cad`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e41d14bbc0d7c5f366f0505bffea36dcc07b0a7e051e5757f3bfab8bfa02e4`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff05668ee8f63f723940795085d559d8dbc223e33475381b9002864f68ff58b`  
		Last Modified: Mon, 08 Sep 2025 23:22:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:d21280d6c72dc2f74d1f6825b4a69bc54f682530fddd54fd562bba8fb3df3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fcb1f04ab003cf2d0dd6a773ff9950670e8884a710f0e071ba0aeed61ab192`

```dockerfile
```

-	Layers:
	-	`sha256:a89ff63ac0bcc4bc2847cfcfa43610cde7b3fa690d3a54f43c2e258e0a8b224a`  
		Last Modified: Tue, 09 Sep 2025 00:02:45 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80812ef99860add889decf87e67f6b742a5a5cf7d168fa554bbf1c7a0be49857`  
		Last Modified: Tue, 09 Sep 2025 00:02:45 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-oracle`

```console
$ docker pull mysql@sha256:9ece5be897e6b58c5756f2f4378bcc2deab42cda5bf363891d141c21b5c6e0de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0df1fa02875e2b873640f068d6cf1ebf9982bded82821465721a503a6e898167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235834455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19538dd7d235eca1d38163bdb4124d5b52a7bcae4ed20c8dd35af64dbd1434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48934deb977008d432d432c942d0c9bf0311e82df69fe878ec98ca432c1275b1`  
		Last Modified: Mon, 08 Sep 2025 22:42:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021b6107b9d0ca5c81a80c275a93fe4a4228d99b7750cc1b8cf22f9041aa2bf2`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16089ebc58ba2085049e3e3e723eb2ed964e8372a9e7854f1a15e680e951`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 6.8 MB (6818663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dcaa70f774ccc9d181d68028676501176ea8e2b3a9e91962ef3bcec1b241d`  
		Last Modified: Mon, 08 Sep 2025 22:42:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a465986d66649506815977bfabe50e4a523971b55edcb36af6211c43f6b609`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa9cc59961edad552866ec7077aa4eefe8dab0dac63791e21ec3cdf0213b6c`  
		Last Modified: Mon, 08 Sep 2025 23:10:08 GMT  
		Size: 49.8 MB (49820062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a27c0ce790fb7bc36776b79407e200eface044a5f5d998e99a99825eef13b97`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390885da77e47ae7ff7bccf3a96b161f38fa9233924d22f92361fce8f13c4079`  
		Last Modified: Mon, 08 Sep 2025 23:09:57 GMT  
		Size: 128.9 MB (128906779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2ca504238ac4a3ac80c3025c09e9e1593957b6b61940b5e58193ee7108faa`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f78235dcb83bdab237d2a5f844020e6ad96e215a36446e3d55bf3a7b10fb65`  
		Last Modified: Mon, 08 Sep 2025 22:43:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bf60ab88436e18691018311be97b29716697da2207fb521e75ef173b8a14f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a573e945f24923ac1241b29ba35ffd6096bc1d60ece181aad5040261e4ef738`

```dockerfile
```

-	Layers:
	-	`sha256:30b6bb4730c967c52f1a703b7ec74602ef6a05d7b1a6673951216b7fbcb91a94`  
		Last Modified: Tue, 09 Sep 2025 00:02:39 GMT  
		Size: 14.5 MB (14528097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c9c8cdcc30e658612165ca5a31cd99fe60d368f07f0084473c887ab18ce37`  
		Last Modified: Tue, 09 Sep 2025 00:02:40 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:44f3046fa0eac90420310151e9959959131c79c7ba7bc670edb7dc1d56cc6d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231621215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5899f96253cec7897b1c32ddcc6f57a4c8fb47bb01d53bf18d2781b3d2dce7a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dfcacb56a5a54ef850255b73ddade5a2fcf52683258ff8f63f58cc435efbbe`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b1f39ad9c5b4a7a28de7069c0b1daa1500ad40bbf0d45dd125518804b45ba`  
		Last Modified: Thu, 21 Aug 2025 21:44:55 GMT  
		Size: 48.7 MB (48677572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e196ab7d9d74832d6a80a475e2af06b5e03e0674a96aac072554941cfe3e6c`  
		Last Modified: Thu, 21 Aug 2025 21:07:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13524f5997c14a8814389dee474a59b93e5e5553bf9596bbadc7fe4b9f166ae5`  
		Last Modified: Thu, 21 Aug 2025 21:45:01 GMT  
		Size: 127.5 MB (127488080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16d0631edced14a95b1b607975b71ae1d4f66b8ae11f09c4a9ba358595f1229`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ebbefeaf6c1ca7184f4be10ba1569ea222109d3b6e7f94655b4445ce79a1f4`  
		Last Modified: Thu, 21 Aug 2025 21:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a81f0012ce016623881070350b9f066ca32c0e717f9d8e6000b62de70452be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ef213789260261eb5b71e3ecc0fb45195b08fcf9298813ac1d740d487e15f1`

```dockerfile
```

-	Layers:
	-	`sha256:0d99250dea0f345c688c802f39338a140b92b19e81ec25ccba59c476881e8c0f`  
		Last Modified: Fri, 22 Aug 2025 00:02:36 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91500571b6a34d8b3ab75a92732cfe47b9c3317e23d5f4300be662c3bdd7e03`  
		Last Modified: Fri, 22 Aug 2025 00:02:38 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-oraclelinux9`

```console
$ docker pull mysql@sha256:9ece5be897e6b58c5756f2f4378bcc2deab42cda5bf363891d141c21b5c6e0de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0df1fa02875e2b873640f068d6cf1ebf9982bded82821465721a503a6e898167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235834455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f19538dd7d235eca1d38163bdb4124d5b52a7bcae4ed20c8dd35af64dbd1434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48934deb977008d432d432c942d0c9bf0311e82df69fe878ec98ca432c1275b1`  
		Last Modified: Mon, 08 Sep 2025 22:42:49 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021b6107b9d0ca5c81a80c275a93fe4a4228d99b7750cc1b8cf22f9041aa2bf2`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16089ebc58ba2085049e3e3e723eb2ed964e8372a9e7854f1a15e680e951`  
		Last Modified: Mon, 08 Sep 2025 23:09:40 GMT  
		Size: 6.8 MB (6818663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dcaa70f774ccc9d181d68028676501176ea8e2b3a9e91962ef3bcec1b241d`  
		Last Modified: Mon, 08 Sep 2025 22:42:58 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a465986d66649506815977bfabe50e4a523971b55edcb36af6211c43f6b609`  
		Last Modified: Mon, 08 Sep 2025 22:43:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fa9cc59961edad552866ec7077aa4eefe8dab0dac63791e21ec3cdf0213b6c`  
		Last Modified: Mon, 08 Sep 2025 23:10:08 GMT  
		Size: 49.8 MB (49820062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a27c0ce790fb7bc36776b79407e200eface044a5f5d998e99a99825eef13b97`  
		Last Modified: Mon, 08 Sep 2025 22:43:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390885da77e47ae7ff7bccf3a96b161f38fa9233924d22f92361fce8f13c4079`  
		Last Modified: Mon, 08 Sep 2025 23:09:57 GMT  
		Size: 128.9 MB (128906779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2ca504238ac4a3ac80c3025c09e9e1593957b6b61940b5e58193ee7108faa`  
		Last Modified: Mon, 08 Sep 2025 22:43:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f78235dcb83bdab237d2a5f844020e6ad96e215a36446e3d55bf3a7b10fb65`  
		Last Modified: Mon, 08 Sep 2025 22:43:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bf60ab88436e18691018311be97b29716697da2207fb521e75ef173b8a14f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a573e945f24923ac1241b29ba35ffd6096bc1d60ece181aad5040261e4ef738`

```dockerfile
```

-	Layers:
	-	`sha256:30b6bb4730c967c52f1a703b7ec74602ef6a05d7b1a6673951216b7fbcb91a94`  
		Last Modified: Tue, 09 Sep 2025 00:02:39 GMT  
		Size: 14.5 MB (14528097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25c9c8cdcc30e658612165ca5a31cd99fe60d368f07f0084473c887ab18ce37`  
		Last Modified: Tue, 09 Sep 2025 00:02:40 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:44f3046fa0eac90420310151e9959959131c79c7ba7bc670edb7dc1d56cc6d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231621215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5899f96253cec7897b1c32ddcc6f57a4c8fb47bb01d53bf18d2781b3d2dce7a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 22:15:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1.el9
# Tue, 22 Jul 2025 22:15:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 22:15:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 22 Jul 2025 22:15:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 22:15:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 22:15:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dfcacb56a5a54ef850255b73ddade5a2fcf52683258ff8f63f58cc435efbbe`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b1f39ad9c5b4a7a28de7069c0b1daa1500ad40bbf0d45dd125518804b45ba`  
		Last Modified: Thu, 21 Aug 2025 21:44:55 GMT  
		Size: 48.7 MB (48677572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e196ab7d9d74832d6a80a475e2af06b5e03e0674a96aac072554941cfe3e6c`  
		Last Modified: Thu, 21 Aug 2025 21:07:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13524f5997c14a8814389dee474a59b93e5e5553bf9596bbadc7fe4b9f166ae5`  
		Last Modified: Thu, 21 Aug 2025 21:45:01 GMT  
		Size: 127.5 MB (127488080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16d0631edced14a95b1b607975b71ae1d4f66b8ae11f09c4a9ba358595f1229`  
		Last Modified: Thu, 21 Aug 2025 21:07:31 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ebbefeaf6c1ca7184f4be10ba1569ea222109d3b6e7f94655b4445ce79a1f4`  
		Last Modified: Thu, 21 Aug 2025 21:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a81f0012ce016623881070350b9f066ca32c0e717f9d8e6000b62de70452be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ef213789260261eb5b71e3ecc0fb45195b08fcf9298813ac1d740d487e15f1`

```dockerfile
```

-	Layers:
	-	`sha256:0d99250dea0f345c688c802f39338a140b92b19e81ec25ccba59c476881e8c0f`  
		Last Modified: Fri, 22 Aug 2025 00:02:36 GMT  
		Size: 14.5 MB (14526448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91500571b6a34d8b3ab75a92732cfe47b9c3317e23d5f4300be662c3bdd7e03`  
		Last Modified: Fri, 22 Aug 2025 00:02:38 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oracle`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oraclelinux9`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oracle`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oraclelinux9`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oracle`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oraclelinux9`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:f65e2eac034463d00c3b1f1f05d5b84171587e7a31db7dfce05d7969d41cad35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:240dbdd43912fd39e8f3dc639089689b508b8483083dc76d4a03de3a3251a6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236815541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb72985bb938a89de9f49e38b08d864d5cd16a71d7cc2131bb5705759c3a8a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0357662693308cd79d9dde75766c7976309ce39f1d5d7b8db58ab741819f0`  
		Last Modified: Mon, 08 Sep 2025 22:42:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328796243e0b1cda6ae546118a08fb6555779ed79af7e8b22327a7fafc6277bf`  
		Last Modified: Mon, 08 Sep 2025 22:42:54 GMT  
		Size: 782.3 KB (782336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cf6c9454cef74eac13b3c45401daf534b3f7295e487fa0f1ab46b477e50c9`  
		Last Modified: Tue, 09 Sep 2025 00:02:24 GMT  
		Size: 6.8 MB (6818672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702ebe6dd8f015a64244c42fecaf58c5dfac4e3b44be8b182f6b5b2ed098381`  
		Last Modified: Mon, 08 Sep 2025 22:42:57 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7894cca000d1f780fcd7afd568bb62adc62ae7b286bd88f9ac6c9b65ade46513`  
		Last Modified: Mon, 08 Sep 2025 22:43:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b5340945f96d3728efd4a61c8935cc9b8b680f30a6651037f92fb99436804f`  
		Last Modified: Tue, 09 Sep 2025 00:02:27 GMT  
		Size: 47.8 MB (47767152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b274c62c3cff97bf3a765a1e0c19b485ed7249a60e9bc1d59a44ebfdd97233`  
		Last Modified: Mon, 08 Sep 2025 22:43:05 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318326631da0031d2bbbccca0fde7425b41bda05c874e2cacab41c91bc7113c3`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 131.9 MB (131940887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582874d217963084d072050a4cd73a3702f97fb909857815b4a26bfe765fb2a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:11 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1d439979703a61dcd0eb26e577f2c5b164f2187f5cc6013d1c00a9131dc9b0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f550ea22b18898ec61433d26b71c1c12d5021cc2403e4584a642ebc2d09263`

```dockerfile
```

-	Layers:
	-	`sha256:9902dbec45a944718eb9b3bada40ecc071ee9787df286b756a9b2f42c933ce79`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 14.8 MB (14804918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782c57399d622ecd87e8e979887d3871918bf441777e72556674d7c327a1993`  
		Last Modified: Tue, 09 Sep 2025 00:02:30 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6368e8abe1ba6c2f5f81fe9ab18e08dfb99448a91775b5f89df713b1d2a8c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232449255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd4be67e75e6b911d39ae63cf443c54318099554595b2c0dcc05d4c2a66413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENV MYSQL_SHELL_VERSION=8.4.6-1.el9
# Tue, 22 Jul 2025 16:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1af5955c5b802b958a56675b9affc38a2dfa2248d2036db56382ec0dd3368c`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27af9b3616319fdf398b75f3f56e9c8c65f09eaaccf2ee05357e0db32c382af`  
		Last Modified: Thu, 21 Aug 2025 20:12:46 GMT  
		Size: 46.7 MB (46653411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df592f759db2d4ced5efd6757e08cddcd91609a23dfeed3065bd812e0c6533`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05071ec68c3fed80b568e5d744cde06e03e2e05f9d2650bdbf05a62d49b68fa0`  
		Last Modified: Thu, 21 Aug 2025 23:21:01 GMT  
		Size: 130.3 MB (130340392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddadd193d15cd72d977f3f72484a9abdf62b2514b8311deb53f75770751d005`  
		Last Modified: Thu, 21 Aug 2025 20:12:42 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:297a766540f4436900b4e7c17962420aeae355642bd546a4ab2ca9efc77bd141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd066b37bb883b8da70cc6661c35b2cb4a5be1a89939800dcfa14ea0eedc4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a7366edbca72d236506dbc127c19010559a66e716cfd0b2d1f531e5d1c64f5d`  
		Last Modified: Fri, 22 Aug 2025 00:02:32 GMT  
		Size: 14.8 MB (14803341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab997bdb6f59ce5469c6aec01ee0a14bc1edeb0f742f20dbd645520e58bfad51`  
		Last Modified: Fri, 22 Aug 2025 00:02:33 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:79d0c4e5095abc78b32a2bd7b4bdaa407e02b5f90eaa63840cbfd8803392f900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5d84b7f27f81300ac1e3243fd294dac525f6858c857edfe255ee20d1bda2adcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275328519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380443b0f0dac49961644a8a48786d1448c4142be9be74f8d8df8c337ab1b1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Mon, 08 Sep 2025 20:09:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Sep 2025 20:09:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:09:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Sep 2025 20:09:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01859c60b4e2a692ef70d5c91c28baf22516970962bf99dab0fbf6ee58395331`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87565b56b57ee54a1c6c80613597ce37e29d093bc5661af77607a1eaad95b482`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f3769f0be64503ae53ceab4179c1c65bed6d303a6329e55061c28f3071651`  
		Last Modified: Tue, 09 Sep 2025 00:01:09 GMT  
		Size: 6.8 MB (6818625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d70b564625bb51eb2eee807280e5cdceaef65de5d24138b8158c5b97d6080b4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d289f7d1ed9b007703129e77fc47b788344d8da9d6a54fdccc2a8ea78fd9d22`  
		Last Modified: Mon, 08 Sep 2025 22:43:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d210a5b69bfed80438c2f7f71b42ba858521b3c97d811ed65cd359f779489eab`  
		Last Modified: Tue, 09 Sep 2025 00:01:26 GMT  
		Size: 49.3 MB (49267174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f5cac1a9e9760f8007c95cc9a6e986a0e6c15b97d05a231713de5a020503a4`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98045e6cd57241627537a64a266ed66d5058135d15590475cc593f8356ff97d2`  
		Last Modified: Tue, 09 Sep 2025 00:03:23 GMT  
		Size: 169.0 MB (168953879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1421f5b704d5566263d9074e3dfac2908d58614a9e15c7e845baff4d4df05b38`  
		Last Modified: Mon, 08 Sep 2025 22:43:29 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:15b44ff233f48b3e37100ab82e405dcb382f8dd2b7f581c805ee74969699e402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812fdfb47775f2b354b913615c45d8570a915c773dd3ee7d58c3c14e3cc0975`

```dockerfile
```

-	Layers:
	-	`sha256:06d0f017e2b49c6db95a9a49fa9eba522e0eaf66466fac3ffadef9f9b114ffaa`  
		Last Modified: Tue, 09 Sep 2025 00:03:18 GMT  
		Size: 17.7 MB (17699285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b0e31e6453f0ab0416ba0ea805b7ac70ca6a1923170092ad52495832e2a00`  
		Last Modified: Tue, 09 Sep 2025 00:03:20 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:93e95d62edb7375158fc7f38bdf051e617a6c601b909c2fb053fe07def749eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270692179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775909ac18966dad262819459871dc5c247f0ca8d0f8e391fbc0a0e4095792b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 22 Jul 2025 16:19:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["/bin/bash"]
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV GOSU_VERSION=1.17
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENV MYSQL_SHELL_VERSION=9.4.0-1.el9
# Tue, 22 Jul 2025 16:19:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 22 Jul 2025 16:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Jul 2025 16:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jul 2025 16:19:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 22 Jul 2025 16:19:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ae8c9f998770f386b491e7ce68f3a723bc4664de920e34b424db9928a2b8`  
		Last Modified: Thu, 21 Aug 2025 20:10:52 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97db50997f07df77c482bfbb0a27db94c04855b5f99cf9c08b9b2688f892c3`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 913.5 KB (913452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07893b7b6550229f3f48d6cfac380579d60fbd0de4175e444353204dd39fd572`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 6.4 MB (6445795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ac0fe1ae14b701f02568df345744b9424b3b8c69bedf9adaeb1f2fab5a46a`  
		Last Modified: Thu, 21 Aug 2025 20:10:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705aca3779f8579552e28c42cd5f59bde8df7854590579392a61c74636cd386`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112df39e0c0171e5c2fd3ba6683933bd1061b8e00ae333093ef137b291a1bd`  
		Last Modified: Thu, 21 Aug 2025 20:11:01 GMT  
		Size: 48.0 MB (48002907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4e3dbbc31fae7425a753a0e67895019e814d6a367c1b1b1ce856cf092787d`  
		Last Modified: Thu, 21 Aug 2025 20:10:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eba9606d89e82f8e2716b04c6c07dbf8e5fb29b38acbd422256bfc2484af5f`  
		Last Modified: Thu, 21 Aug 2025 22:06:54 GMT  
		Size: 167.2 MB (167233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b88c5f89df0192aa9e02d0dd87b587a3f7eaaa22b2758b238550112206248`  
		Last Modified: Thu, 21 Aug 2025 20:10:55 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:044aac32dadb8c575046f67eeed2d8d92b3fcb4574e5dbee0dc6c2366d916f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e7aa649c7763551530ec55fc37dabb78e0e7ed1e0219d6b6fdb4797e1eff10`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1b8161776bf227a6ae2d07bde154e18a312344a4e6e1c2386ae3829742358`  
		Last Modified: Fri, 22 Aug 2025 00:02:57 GMT  
		Size: 17.7 MB (17694431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eacd3227abfeb8887a33151a5ec6ba7a87239f9f0a7481d5c9a5f3a6e99d11c`  
		Last Modified: Fri, 22 Aug 2025 00:02:58 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
