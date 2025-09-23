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
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:250030e1f5660193c48b146214f6cc726cd929e71fd3a37bbdcff4c0754dd488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:1b5f6f1c80a24e2a853d6c073b5b80762165b6396c1311714fcb3cf6f6ee5254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ba685cf605c5887cce92c568538aeec7969eaf0f3553f66442b296d5b2a8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc4d6c5a4ee0e8c36f827a99b8882679297728b8f52f639fae9263159867eae`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659638c120e9acdeef34043175abf577e9d69692c1e06078e5707e77a5063b41`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 782.3 KB (782339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a270e63f90d6ff0443fb14468d3fbf3b21285659f9d06e666bb32e10c8fdc`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 6.8 MB (6820284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9659c06df790b279f2fe963f7ce85fd11a0a854bce91697439c2f8382301df`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c072a1db59e7b0c65485f1cdfcf00faf10799ba3ae69a176337f9e01e43a6`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb688bb168b4981a77aaecee8a868f08205bd4e738d6f88790f4f8a529f05fa`  
		Last Modified: Tue, 23 Sep 2025 02:52:20 GMT  
		Size: 49.8 MB (49837975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046d4330c373c717a984f31a0b8979cb95103daac0e17b85cd4085d6742ab5b`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256c553a5f43ba1ecbb6c118b049aebc687255f3ecb1b854cc5071c375943398`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 128.9 MB (128928162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2150a5aa6764b983bee1e4e7a4cb617d3d5052a2f25f8c7cc7bf2e3b5d26b66`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19791c1430e6766420d131f763275ab5c4b6eae9a5defa2d4a1d52607e46009`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:258cdcbc161a14b8ce13c18f13375d8f992feccc76ce404a655de9e34da21178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b34d4624e316bfdc0e3fd48b1b6a85bd4938800a934b5b08c6f8db41b10964`

```dockerfile
```

-	Layers:
	-	`sha256:4cf66ab8e6089134ae92b5df2611a66b29a0c5c056f2186b6c1f7b9cb8beaed6`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3a2b19ad5da1c43a6b68ee695861491d0820c06e3ae66bea5c8e1e8acedccb`  
		Last Modified: Tue, 23 Sep 2025 06:02:30 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:eba9cd525fbf9b7f9d773dc03c37a37a7d4588ced932defe1b701f89a3dfc97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6655f4b3c23e1f9e70065bf3ccbcced3810d0692b4cef1768361803e76252b50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45394b6e59d93dd6ceceb0074c8b166008f7964f2024c4321583e74da2f44bb7`  
		Last Modified: Mon, 22 Sep 2025 21:14:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3097d73b0b3a208a4a7a3e763afbb1a39658f35b081191802b493be87ac5562`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a494642a71811b077e49cd63af0804f63e139490ce1898bf3b7a9f303f2cc7`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 6.4 MB (6445544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d10c1c7d3fd7e4fbb763d572141c4a14e68e2bbb09cc09d88da3e6ece38fa9`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c605c9229a647d34e45d05eee2ca99d67eaa77d0ce2d0e1bf8d80dc3e062494a`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12195581addbe4c53de9cc7f43b1b5c5a51034f422888ff214994124ad8aeb4a`  
		Last Modified: Mon, 22 Sep 2025 21:14:21 GMT  
		Size: 48.7 MB (48694893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444a9bcea72f7da42321411052b38f00a1ac2fc603c1a05e3c7e688db3cf78b4`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d433be77e07dfdb7095c9d3407dac491ca91c96d3e183786f7fc67d3492f6ec4`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 127.5 MB (127506018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ce78738d988fbc22e3f33f83596b199534bb6f7b776587bd4aa5a1bbf13f7`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5679a87503ed777e838e2413d086161632eeb24871e7bfc3e0bea04947b3be`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:7af1bcb37a15930afe9e2616d36702a52cbffc379086569de321dacd1fec2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60af38484f935fcf4021797a671bdec034180aae5594cd674f0a34175b155ab`

```dockerfile
```

-	Layers:
	-	`sha256:2bf2fa084a21b68bae9d3914c10defbceb8d63dd4fca5b64d5fe93028bcf7057`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af249fb4b854066cad8d8d22d4dccbd6e636bfc108342e7a5978ec9a44a84b6`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
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
$ docker pull mysql@sha256:250030e1f5660193c48b146214f6cc726cd929e71fd3a37bbdcff4c0754dd488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1b5f6f1c80a24e2a853d6c073b5b80762165b6396c1311714fcb3cf6f6ee5254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ba685cf605c5887cce92c568538aeec7969eaf0f3553f66442b296d5b2a8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc4d6c5a4ee0e8c36f827a99b8882679297728b8f52f639fae9263159867eae`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659638c120e9acdeef34043175abf577e9d69692c1e06078e5707e77a5063b41`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 782.3 KB (782339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a270e63f90d6ff0443fb14468d3fbf3b21285659f9d06e666bb32e10c8fdc`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 6.8 MB (6820284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9659c06df790b279f2fe963f7ce85fd11a0a854bce91697439c2f8382301df`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c072a1db59e7b0c65485f1cdfcf00faf10799ba3ae69a176337f9e01e43a6`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb688bb168b4981a77aaecee8a868f08205bd4e738d6f88790f4f8a529f05fa`  
		Last Modified: Tue, 23 Sep 2025 02:52:20 GMT  
		Size: 49.8 MB (49837975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046d4330c373c717a984f31a0b8979cb95103daac0e17b85cd4085d6742ab5b`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256c553a5f43ba1ecbb6c118b049aebc687255f3ecb1b854cc5071c375943398`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 128.9 MB (128928162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2150a5aa6764b983bee1e4e7a4cb617d3d5052a2f25f8c7cc7bf2e3b5d26b66`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19791c1430e6766420d131f763275ab5c4b6eae9a5defa2d4a1d52607e46009`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:258cdcbc161a14b8ce13c18f13375d8f992feccc76ce404a655de9e34da21178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b34d4624e316bfdc0e3fd48b1b6a85bd4938800a934b5b08c6f8db41b10964`

```dockerfile
```

-	Layers:
	-	`sha256:4cf66ab8e6089134ae92b5df2611a66b29a0c5c056f2186b6c1f7b9cb8beaed6`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3a2b19ad5da1c43a6b68ee695861491d0820c06e3ae66bea5c8e1e8acedccb`  
		Last Modified: Tue, 23 Sep 2025 06:02:30 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:eba9cd525fbf9b7f9d773dc03c37a37a7d4588ced932defe1b701f89a3dfc97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6655f4b3c23e1f9e70065bf3ccbcced3810d0692b4cef1768361803e76252b50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45394b6e59d93dd6ceceb0074c8b166008f7964f2024c4321583e74da2f44bb7`  
		Last Modified: Mon, 22 Sep 2025 21:14:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3097d73b0b3a208a4a7a3e763afbb1a39658f35b081191802b493be87ac5562`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a494642a71811b077e49cd63af0804f63e139490ce1898bf3b7a9f303f2cc7`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 6.4 MB (6445544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d10c1c7d3fd7e4fbb763d572141c4a14e68e2bbb09cc09d88da3e6ece38fa9`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c605c9229a647d34e45d05eee2ca99d67eaa77d0ce2d0e1bf8d80dc3e062494a`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12195581addbe4c53de9cc7f43b1b5c5a51034f422888ff214994124ad8aeb4a`  
		Last Modified: Mon, 22 Sep 2025 21:14:21 GMT  
		Size: 48.7 MB (48694893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444a9bcea72f7da42321411052b38f00a1ac2fc603c1a05e3c7e688db3cf78b4`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d433be77e07dfdb7095c9d3407dac491ca91c96d3e183786f7fc67d3492f6ec4`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 127.5 MB (127506018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ce78738d988fbc22e3f33f83596b199534bb6f7b776587bd4aa5a1bbf13f7`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5679a87503ed777e838e2413d086161632eeb24871e7bfc3e0bea04947b3be`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7af1bcb37a15930afe9e2616d36702a52cbffc379086569de321dacd1fec2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60af38484f935fcf4021797a671bdec034180aae5594cd674f0a34175b155ab`

```dockerfile
```

-	Layers:
	-	`sha256:2bf2fa084a21b68bae9d3914c10defbceb8d63dd4fca5b64d5fe93028bcf7057`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af249fb4b854066cad8d8d22d4dccbd6e636bfc108342e7a5978ec9a44a84b6`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:250030e1f5660193c48b146214f6cc726cd929e71fd3a37bbdcff4c0754dd488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1b5f6f1c80a24e2a853d6c073b5b80762165b6396c1311714fcb3cf6f6ee5254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ba685cf605c5887cce92c568538aeec7969eaf0f3553f66442b296d5b2a8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc4d6c5a4ee0e8c36f827a99b8882679297728b8f52f639fae9263159867eae`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659638c120e9acdeef34043175abf577e9d69692c1e06078e5707e77a5063b41`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 782.3 KB (782339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a270e63f90d6ff0443fb14468d3fbf3b21285659f9d06e666bb32e10c8fdc`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 6.8 MB (6820284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9659c06df790b279f2fe963f7ce85fd11a0a854bce91697439c2f8382301df`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c072a1db59e7b0c65485f1cdfcf00faf10799ba3ae69a176337f9e01e43a6`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb688bb168b4981a77aaecee8a868f08205bd4e738d6f88790f4f8a529f05fa`  
		Last Modified: Tue, 23 Sep 2025 02:52:20 GMT  
		Size: 49.8 MB (49837975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046d4330c373c717a984f31a0b8979cb95103daac0e17b85cd4085d6742ab5b`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256c553a5f43ba1ecbb6c118b049aebc687255f3ecb1b854cc5071c375943398`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 128.9 MB (128928162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2150a5aa6764b983bee1e4e7a4cb617d3d5052a2f25f8c7cc7bf2e3b5d26b66`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19791c1430e6766420d131f763275ab5c4b6eae9a5defa2d4a1d52607e46009`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:258cdcbc161a14b8ce13c18f13375d8f992feccc76ce404a655de9e34da21178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b34d4624e316bfdc0e3fd48b1b6a85bd4938800a934b5b08c6f8db41b10964`

```dockerfile
```

-	Layers:
	-	`sha256:4cf66ab8e6089134ae92b5df2611a66b29a0c5c056f2186b6c1f7b9cb8beaed6`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3a2b19ad5da1c43a6b68ee695861491d0820c06e3ae66bea5c8e1e8acedccb`  
		Last Modified: Tue, 23 Sep 2025 06:02:30 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:eba9cd525fbf9b7f9d773dc03c37a37a7d4588ced932defe1b701f89a3dfc97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6655f4b3c23e1f9e70065bf3ccbcced3810d0692b4cef1768361803e76252b50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45394b6e59d93dd6ceceb0074c8b166008f7964f2024c4321583e74da2f44bb7`  
		Last Modified: Mon, 22 Sep 2025 21:14:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3097d73b0b3a208a4a7a3e763afbb1a39658f35b081191802b493be87ac5562`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a494642a71811b077e49cd63af0804f63e139490ce1898bf3b7a9f303f2cc7`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 6.4 MB (6445544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d10c1c7d3fd7e4fbb763d572141c4a14e68e2bbb09cc09d88da3e6ece38fa9`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c605c9229a647d34e45d05eee2ca99d67eaa77d0ce2d0e1bf8d80dc3e062494a`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12195581addbe4c53de9cc7f43b1b5c5a51034f422888ff214994124ad8aeb4a`  
		Last Modified: Mon, 22 Sep 2025 21:14:21 GMT  
		Size: 48.7 MB (48694893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444a9bcea72f7da42321411052b38f00a1ac2fc603c1a05e3c7e688db3cf78b4`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d433be77e07dfdb7095c9d3407dac491ca91c96d3e183786f7fc67d3492f6ec4`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 127.5 MB (127506018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ce78738d988fbc22e3f33f83596b199534bb6f7b776587bd4aa5a1bbf13f7`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5679a87503ed777e838e2413d086161632eeb24871e7bfc3e0bea04947b3be`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7af1bcb37a15930afe9e2616d36702a52cbffc379086569de321dacd1fec2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60af38484f935fcf4021797a671bdec034180aae5594cd674f0a34175b155ab`

```dockerfile
```

-	Layers:
	-	`sha256:2bf2fa084a21b68bae9d3914c10defbceb8d63dd4fca5b64d5fe93028bcf7057`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af249fb4b854066cad8d8d22d4dccbd6e636bfc108342e7a5978ec9a44a84b6`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43`

```console
$ docker pull mysql@sha256:250030e1f5660193c48b146214f6cc726cd929e71fd3a37bbdcff4c0754dd488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43` - linux; amd64

```console
$ docker pull mysql@sha256:1b5f6f1c80a24e2a853d6c073b5b80762165b6396c1311714fcb3cf6f6ee5254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ba685cf605c5887cce92c568538aeec7969eaf0f3553f66442b296d5b2a8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc4d6c5a4ee0e8c36f827a99b8882679297728b8f52f639fae9263159867eae`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659638c120e9acdeef34043175abf577e9d69692c1e06078e5707e77a5063b41`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 782.3 KB (782339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a270e63f90d6ff0443fb14468d3fbf3b21285659f9d06e666bb32e10c8fdc`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 6.8 MB (6820284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9659c06df790b279f2fe963f7ce85fd11a0a854bce91697439c2f8382301df`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c072a1db59e7b0c65485f1cdfcf00faf10799ba3ae69a176337f9e01e43a6`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb688bb168b4981a77aaecee8a868f08205bd4e738d6f88790f4f8a529f05fa`  
		Last Modified: Tue, 23 Sep 2025 02:52:20 GMT  
		Size: 49.8 MB (49837975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046d4330c373c717a984f31a0b8979cb95103daac0e17b85cd4085d6742ab5b`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256c553a5f43ba1ecbb6c118b049aebc687255f3ecb1b854cc5071c375943398`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 128.9 MB (128928162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2150a5aa6764b983bee1e4e7a4cb617d3d5052a2f25f8c7cc7bf2e3b5d26b66`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19791c1430e6766420d131f763275ab5c4b6eae9a5defa2d4a1d52607e46009`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:258cdcbc161a14b8ce13c18f13375d8f992feccc76ce404a655de9e34da21178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b34d4624e316bfdc0e3fd48b1b6a85bd4938800a934b5b08c6f8db41b10964`

```dockerfile
```

-	Layers:
	-	`sha256:4cf66ab8e6089134ae92b5df2611a66b29a0c5c056f2186b6c1f7b9cb8beaed6`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3a2b19ad5da1c43a6b68ee695861491d0820c06e3ae66bea5c8e1e8acedccb`  
		Last Modified: Tue, 23 Sep 2025 06:02:30 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:eba9cd525fbf9b7f9d773dc03c37a37a7d4588ced932defe1b701f89a3dfc97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6655f4b3c23e1f9e70065bf3ccbcced3810d0692b4cef1768361803e76252b50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45394b6e59d93dd6ceceb0074c8b166008f7964f2024c4321583e74da2f44bb7`  
		Last Modified: Mon, 22 Sep 2025 21:14:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3097d73b0b3a208a4a7a3e763afbb1a39658f35b081191802b493be87ac5562`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a494642a71811b077e49cd63af0804f63e139490ce1898bf3b7a9f303f2cc7`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 6.4 MB (6445544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d10c1c7d3fd7e4fbb763d572141c4a14e68e2bbb09cc09d88da3e6ece38fa9`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c605c9229a647d34e45d05eee2ca99d67eaa77d0ce2d0e1bf8d80dc3e062494a`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12195581addbe4c53de9cc7f43b1b5c5a51034f422888ff214994124ad8aeb4a`  
		Last Modified: Mon, 22 Sep 2025 21:14:21 GMT  
		Size: 48.7 MB (48694893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444a9bcea72f7da42321411052b38f00a1ac2fc603c1a05e3c7e688db3cf78b4`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d433be77e07dfdb7095c9d3407dac491ca91c96d3e183786f7fc67d3492f6ec4`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 127.5 MB (127506018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ce78738d988fbc22e3f33f83596b199534bb6f7b776587bd4aa5a1bbf13f7`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5679a87503ed777e838e2413d086161632eeb24871e7bfc3e0bea04947b3be`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43` - unknown; unknown

```console
$ docker pull mysql@sha256:7af1bcb37a15930afe9e2616d36702a52cbffc379086569de321dacd1fec2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60af38484f935fcf4021797a671bdec034180aae5594cd674f0a34175b155ab`

```dockerfile
```

-	Layers:
	-	`sha256:2bf2fa084a21b68bae9d3914c10defbceb8d63dd4fca5b64d5fe93028bcf7057`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af249fb4b854066cad8d8d22d4dccbd6e636bfc108342e7a5978ec9a44a84b6`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
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
$ docker pull mysql@sha256:250030e1f5660193c48b146214f6cc726cd929e71fd3a37bbdcff4c0754dd488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1b5f6f1c80a24e2a853d6c073b5b80762165b6396c1311714fcb3cf6f6ee5254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ba685cf605c5887cce92c568538aeec7969eaf0f3553f66442b296d5b2a8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc4d6c5a4ee0e8c36f827a99b8882679297728b8f52f639fae9263159867eae`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659638c120e9acdeef34043175abf577e9d69692c1e06078e5707e77a5063b41`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 782.3 KB (782339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a270e63f90d6ff0443fb14468d3fbf3b21285659f9d06e666bb32e10c8fdc`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 6.8 MB (6820284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9659c06df790b279f2fe963f7ce85fd11a0a854bce91697439c2f8382301df`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c072a1db59e7b0c65485f1cdfcf00faf10799ba3ae69a176337f9e01e43a6`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb688bb168b4981a77aaecee8a868f08205bd4e738d6f88790f4f8a529f05fa`  
		Last Modified: Tue, 23 Sep 2025 02:52:20 GMT  
		Size: 49.8 MB (49837975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046d4330c373c717a984f31a0b8979cb95103daac0e17b85cd4085d6742ab5b`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256c553a5f43ba1ecbb6c118b049aebc687255f3ecb1b854cc5071c375943398`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 128.9 MB (128928162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2150a5aa6764b983bee1e4e7a4cb617d3d5052a2f25f8c7cc7bf2e3b5d26b66`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19791c1430e6766420d131f763275ab5c4b6eae9a5defa2d4a1d52607e46009`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:258cdcbc161a14b8ce13c18f13375d8f992feccc76ce404a655de9e34da21178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b34d4624e316bfdc0e3fd48b1b6a85bd4938800a934b5b08c6f8db41b10964`

```dockerfile
```

-	Layers:
	-	`sha256:4cf66ab8e6089134ae92b5df2611a66b29a0c5c056f2186b6c1f7b9cb8beaed6`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3a2b19ad5da1c43a6b68ee695861491d0820c06e3ae66bea5c8e1e8acedccb`  
		Last Modified: Tue, 23 Sep 2025 06:02:30 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:eba9cd525fbf9b7f9d773dc03c37a37a7d4588ced932defe1b701f89a3dfc97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6655f4b3c23e1f9e70065bf3ccbcced3810d0692b4cef1768361803e76252b50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45394b6e59d93dd6ceceb0074c8b166008f7964f2024c4321583e74da2f44bb7`  
		Last Modified: Mon, 22 Sep 2025 21:14:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3097d73b0b3a208a4a7a3e763afbb1a39658f35b081191802b493be87ac5562`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a494642a71811b077e49cd63af0804f63e139490ce1898bf3b7a9f303f2cc7`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 6.4 MB (6445544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d10c1c7d3fd7e4fbb763d572141c4a14e68e2bbb09cc09d88da3e6ece38fa9`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c605c9229a647d34e45d05eee2ca99d67eaa77d0ce2d0e1bf8d80dc3e062494a`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12195581addbe4c53de9cc7f43b1b5c5a51034f422888ff214994124ad8aeb4a`  
		Last Modified: Mon, 22 Sep 2025 21:14:21 GMT  
		Size: 48.7 MB (48694893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444a9bcea72f7da42321411052b38f00a1ac2fc603c1a05e3c7e688db3cf78b4`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d433be77e07dfdb7095c9d3407dac491ca91c96d3e183786f7fc67d3492f6ec4`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 127.5 MB (127506018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ce78738d988fbc22e3f33f83596b199534bb6f7b776587bd4aa5a1bbf13f7`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5679a87503ed777e838e2413d086161632eeb24871e7bfc3e0bea04947b3be`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7af1bcb37a15930afe9e2616d36702a52cbffc379086569de321dacd1fec2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60af38484f935fcf4021797a671bdec034180aae5594cd674f0a34175b155ab`

```dockerfile
```

-	Layers:
	-	`sha256:2bf2fa084a21b68bae9d3914c10defbceb8d63dd4fca5b64d5fe93028bcf7057`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af249fb4b854066cad8d8d22d4dccbd6e636bfc108342e7a5978ec9a44a84b6`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.43-oraclelinux9`

```console
$ docker pull mysql@sha256:250030e1f5660193c48b146214f6cc726cd929e71fd3a37bbdcff4c0754dd488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.43-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1b5f6f1c80a24e2a853d6c073b5b80762165b6396c1311714fcb3cf6f6ee5254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235875342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ba685cf605c5887cce92c568538aeec7969eaf0f3553f66442b296d5b2a8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc4d6c5a4ee0e8c36f827a99b8882679297728b8f52f639fae9263159867eae`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659638c120e9acdeef34043175abf577e9d69692c1e06078e5707e77a5063b41`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 782.3 KB (782339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a270e63f90d6ff0443fb14468d3fbf3b21285659f9d06e666bb32e10c8fdc`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 6.8 MB (6820284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9659c06df790b279f2fe963f7ce85fd11a0a854bce91697439c2f8382301df`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49c072a1db59e7b0c65485f1cdfcf00faf10799ba3ae69a176337f9e01e43a6`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb688bb168b4981a77aaecee8a868f08205bd4e738d6f88790f4f8a529f05fa`  
		Last Modified: Tue, 23 Sep 2025 02:52:20 GMT  
		Size: 49.8 MB (49837975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046d4330c373c717a984f31a0b8979cb95103daac0e17b85cd4085d6742ab5b`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256c553a5f43ba1ecbb6c118b049aebc687255f3ecb1b854cc5071c375943398`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 128.9 MB (128928162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2150a5aa6764b983bee1e4e7a4cb617d3d5052a2f25f8c7cc7bf2e3b5d26b66`  
		Last Modified: Tue, 23 Sep 2025 02:52:16 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19791c1430e6766420d131f763275ab5c4b6eae9a5defa2d4a1d52607e46009`  
		Last Modified: Tue, 23 Sep 2025 02:52:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:258cdcbc161a14b8ce13c18f13375d8f992feccc76ce404a655de9e34da21178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b34d4624e316bfdc0e3fd48b1b6a85bd4938800a934b5b08c6f8db41b10964`

```dockerfile
```

-	Layers:
	-	`sha256:4cf66ab8e6089134ae92b5df2611a66b29a0c5c056f2186b6c1f7b9cb8beaed6`  
		Last Modified: Tue, 23 Sep 2025 06:02:29 GMT  
		Size: 14.5 MB (14528105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3a2b19ad5da1c43a6b68ee695861491d0820c06e3ae66bea5c8e1e8acedccb`  
		Last Modified: Tue, 23 Sep 2025 06:02:30 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.43-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:eba9cd525fbf9b7f9d773dc03c37a37a7d4588ced932defe1b701f89a3dfc97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231481156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6655f4b3c23e1f9e70065bf3ccbcced3810d0692b4cef1768361803e76252b50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45394b6e59d93dd6ceceb0074c8b166008f7964f2024c4321583e74da2f44bb7`  
		Last Modified: Mon, 22 Sep 2025 21:14:09 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3097d73b0b3a208a4a7a3e763afbb1a39658f35b081191802b493be87ac5562`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a494642a71811b077e49cd63af0804f63e139490ce1898bf3b7a9f303f2cc7`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 6.4 MB (6445544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d10c1c7d3fd7e4fbb763d572141c4a14e68e2bbb09cc09d88da3e6ece38fa9`  
		Last Modified: Mon, 22 Sep 2025 21:14:10 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c605c9229a647d34e45d05eee2ca99d67eaa77d0ce2d0e1bf8d80dc3e062494a`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12195581addbe4c53de9cc7f43b1b5c5a51034f422888ff214994124ad8aeb4a`  
		Last Modified: Mon, 22 Sep 2025 21:14:21 GMT  
		Size: 48.7 MB (48694893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444a9bcea72f7da42321411052b38f00a1ac2fc603c1a05e3c7e688db3cf78b4`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d433be77e07dfdb7095c9d3407dac491ca91c96d3e183786f7fc67d3492f6ec4`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 127.5 MB (127506018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ce78738d988fbc22e3f33f83596b199534bb6f7b776587bd4aa5a1bbf13f7`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5679a87503ed777e838e2413d086161632eeb24871e7bfc3e0bea04947b3be`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.43-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7af1bcb37a15930afe9e2616d36702a52cbffc379086569de321dacd1fec2663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14561654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60af38484f935fcf4021797a671bdec034180aae5594cd674f0a34175b155ab`

```dockerfile
```

-	Layers:
	-	`sha256:2bf2fa084a21b68bae9d3914c10defbceb8d63dd4fca5b64d5fe93028bcf7057`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 14.5 MB (14526452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af249fb4b854066cad8d8d22d4dccbd6e636bfc108342e7a5978ec9a44a84b6`  
		Last Modified: Tue, 23 Sep 2025 00:02:37 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oracle`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.6-oraclelinux9`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oracle`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4-oraclelinux9`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oracle`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.4.0-oraclelinux9`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.4.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.4.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:70fe679fe46969324983655f9d02c90ab97499bc48ec98598e8fe27e91fe51f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5aa7f9d722f749672e9d48ad6f2d56dc2642b3754885602fcf0c453ee679426f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236858191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e436a245c09e1a78c12fac6ff6bd5a37c901786755dbbd951cb6067ea2c0adf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d396d56c0de4a8b5a0a640f4ff5c2cf7c8ff53250499c848700fc00a9c8b76`  
		Last Modified: Tue, 23 Sep 2025 02:52:01 GMT  
		Size: 886.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560e6225696359e873abc871ed662f34fd0fa7882ce9945d3f14908fee00b290`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7116617a71a67e36480cdbd6ec9bbe5a386c0501a191f9e1cfeb3fb799b739e`  
		Last Modified: Tue, 23 Sep 2025 02:52:03 GMT  
		Size: 6.8 MB (6820257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdba291c4e7d36ff03261fb2703ee50697314566dc6283276b469dd02d53102c`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0f8ea31c54cef1cae21c1c13715d31143071b3010923445efbcb9e2fc48cf`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a56c1b1d9e623ed89c2b4cabbd7115feb7534374a26240e1c90f79c3e4953e`  
		Last Modified: Tue, 23 Sep 2025 02:52:06 GMT  
		Size: 47.8 MB (47786372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1beaec8325fb719c95de0669a93eefea15f4dba80d4a240dd451735ce7ff4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc8f737ad53ebbce73cae0fb82eaa2065152613997fe5aeb894a59029c189a`  
		Last Modified: Tue, 23 Sep 2025 03:10:20 GMT  
		Size: 132.0 MB (131962756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc9e4250cdbc93de3c8b02f8673592992f44649746a180576bd00122c97f4`  
		Last Modified: Tue, 23 Sep 2025 02:52:02 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7a8d23e183811d9ff126a6f01a173509cf24b7ead9abb1630691bbdff2c14cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4cf7952ed8ab69fce7bf214aad357a6ca253f9d573d6dcc15ac23132a18426`

```dockerfile
```

-	Layers:
	-	`sha256:a93f8755e53e1b5cdc04d572ba2a8177f623ca0977a9a6455f2023319ba3b0c6`  
		Last Modified: Tue, 23 Sep 2025 06:02:27 GMT  
		Size: 14.8 MB (14804926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eac1a9eb79b77fc71158ef85bcf3bbe695ebbd2048a003552a0d589044a7689`  
		Last Modified: Tue, 23 Sep 2025 06:02:28 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:edd67ae22d236181c5c02881a188fa285d12d9b51a074ffd19cfb742f199a47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232309691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825b7f7a9424db55f772773500cb6833402bd5fa9291252f13931ebb07653c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a96f265f3fda092530bfc39d09f74d997f36956b66490ae6898335c6fd607f`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174226e780c721e7268bfa66bd75136a5051c4b8124d4a6e3d39027c0985a035`  
		Last Modified: Mon, 22 Sep 2025 21:14:11 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fdcf21153ca4bf268b41fdf9c541edc157bdd3b2ded3a303a14c448d5f82d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 6.4 MB (6445455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cd61acfade0bfd7dbbc9703bec40372c8383bbee16d323d5b91464f4151ea`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d1fee1e0dea4cefe98a8aebc8018762c98b7e043a88dbba3b0e973c1d32d9`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00161466cbe75467f3e003b67da39064cdaea5a130ba764a215f8fa1f6684a5f`  
		Last Modified: Mon, 22 Sep 2025 21:14:23 GMT  
		Size: 46.7 MB (46672622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4941c1bf292c551256d247be95e2bc2d227743a9f601b44385507fe7ef182a9c`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f18dc7365a206f81f32f0e64978a1e95c6f581e23e8b49d5345adcafcd4f9`  
		Last Modified: Mon, 22 Sep 2025 21:15:25 GMT  
		Size: 130.4 MB (130357036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a74b84e979aab9520e81679d9c5bada9c18671de54c6d6be70e9d3e8c810a1`  
		Last Modified: Mon, 22 Sep 2025 21:14:15 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fbf8bc43f92823a29185f324713e2003a6eef40d76f08387b52441bec0c7fd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14837901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2db4873bb02ea7a4eef5f1d0803cfc0f0f34f4a59739d4945291444f93032d`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9d3a692a6b0cc269f46b25f82f0632cc4da30435e8fb61d0dcf554c6b8a0`  
		Last Modified: Tue, 23 Sep 2025 00:02:27 GMT  
		Size: 14.8 MB (14803345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b691dcd118c94bb28898be28ad7dfea451b16e62f852fbf91836abf678278d29`  
		Last Modified: Tue, 23 Sep 2025 00:02:28 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:6ca0f7c0b0fefa59efffacbbfbc5399d3079493a7404146ca2a3ee2c2d3090e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:bc8558595f075880f11d0c98e5a08e10f5d80741dcc1ee8c662ce12383ec31e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275364479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701c61006220558cf5359cbd8f227501657047687fcc8916fadad5647a245d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb39ea9eb78894030098510f1fb1065ed766ac231bbc8b59ace126b0e0f10b`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bc901cd7579ec1480e3c5922d9c14cd7678d9ae900d486ec7c8c7403cf186a`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 782.3 KB (782337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef95293edcc6c867dc59582a3a570ce517b8c900c74a16e901be88fe9fe4f61`  
		Last Modified: Tue, 23 Sep 2025 02:50:21 GMT  
		Size: 6.8 MB (6820265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b74ec21328ed589f2c582a227b9001ee46596813a52a6c9364eba34b93b5ac`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0382fa00b86e2ef89dd63b259d75dd5a7ae09e6a3b5cb309b2f026616a1bed16`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2c06ece724ecbb728b6db7f194625b99f3632bebbf0dffdc0f9c8657a0443`  
		Last Modified: Tue, 23 Sep 2025 02:50:23 GMT  
		Size: 49.3 MB (49286550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c033455d26fe93037b52e6a0193372e71f2385360672421a2d625f0f0d9407`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8cf8cbef82020956468970cdb1e54832952733dbea80a28e89767ceecc7b3`  
		Last Modified: Tue, 23 Sep 2025 02:51:26 GMT  
		Size: 169.0 MB (168968845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76ce42d6a1517e13e0cb41ded69399fa1bb3097af743ad5f33052787d9eff9`  
		Last Modified: Tue, 23 Sep 2025 02:50:20 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:741c74932061f7275e3785eefae21b1b9491e28ccdea5db9fc610f2e4b1f18de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19edbc050dbada63d0da5f33a1427389f4ef43c5db38d4a2a3ffa0c00351059a`

```dockerfile
```

-	Layers:
	-	`sha256:efe0e3f017c7b676d38b7b5e4836973524ae21cc4ac827d97688ac3d7dcbfbeb`  
		Last Modified: Tue, 23 Sep 2025 06:02:59 GMT  
		Size: 17.7 MB (17699293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea462bb5c1d9aefe1b950b34c11150295a150329add5bb1618d34fdc4f6abc`  
		Last Modified: Tue, 23 Sep 2025 06:03:00 GMT  
		Size: 35.3 KB (35317 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:87cd9b7749fc36f4e3fdb9e7b9b1d1beef6d0fcdcc86a1dc4cbf95dc2b374a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270561286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e302fae3e0da657d137e4e4f397f40fd8db599e49e594f0f63b7bb94aa5b231c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Sep 2025 20:09:09 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 08 Sep 2025 20:09:09 GMT
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
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b8a0502dd3d554d2fa2ed461350d19a77e4924952a3c6dd78be0c97d78854f`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506f059fc2ef78b499713c5ae44e8cea7c807b10835f256cb4dae21909421980`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 736.8 KB (736806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dcc3de3279ef818caf4679d2d9f4f6703ca1853fde7edf46534e2d33a5c155`  
		Last Modified: Mon, 22 Sep 2025 21:14:14 GMT  
		Size: 6.4 MB (6445287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e07b4f9ab9a52af0e5bd612945dcc18a201983131ae7da2bb130a5f7dc65d2`  
		Last Modified: Mon, 22 Sep 2025 21:14:12 GMT  
		Size: 2.6 KB (2601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae09da59b9d29b41672cb61d0fa62bbf9e409fa2460e268a9ae87a9f7240408`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc640df1873273a2c4270af0c47c2ad3e89eb0e27af314d1554560f7882ee52`  
		Last Modified: Mon, 22 Sep 2025 21:14:19 GMT  
		Size: 48.0 MB (48019788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac245f230a2fd001f24602fb220fbeea7a31f9fa0552dcebfeacc8362902a`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754509197b016198ea7ebf9c0e4fa8503a144054606f8ebff22abaafca5cdc43`  
		Last Modified: Mon, 22 Sep 2025 22:38:18 GMT  
		Size: 167.3 MB (167261626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3848009b0e319bb5ab216ef068dc2ebb97c0789be82df5bce069a0670e1f3e`  
		Last Modified: Mon, 22 Sep 2025 21:14:13 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3136a10e1f0f9b82327e65d17482ee81dae708df3602f116aa020395701b3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17730094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840403503fdb614c72d10cceeb0c01306229f8134daa89b4989fb401a009bc44`

```dockerfile
```

-	Layers:
	-	`sha256:199a34f1e6c65eb3b53588261f9889b1347e45a308b27f86f18d17816a9bcc53`  
		Last Modified: Tue, 23 Sep 2025 00:03:13 GMT  
		Size: 17.7 MB (17694435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed51c5ceffee6ad4b1aaf7a1aa4af7d35c83c42c7a313dc28f2efaf42626442`  
		Last Modified: Tue, 23 Sep 2025 00:03:14 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
