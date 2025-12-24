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
-	[`mysql:8.0.44`](#mysql8044)
-	[`mysql:8.0.44-bookworm`](#mysql8044-bookworm)
-	[`mysql:8.0.44-debian`](#mysql8044-debian)
-	[`mysql:8.0.44-oracle`](#mysql8044-oracle)
-	[`mysql:8.0.44-oraclelinux9`](#mysql8044-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.7`](#mysql847)
-	[`mysql:8.4.7-oracle`](#mysql847-oracle)
-	[`mysql:8.4.7-oraclelinux9`](#mysql847-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.5`](#mysql95)
-	[`mysql:9.5-oracle`](#mysql95-oracle)
-	[`mysql:9.5-oraclelinux9`](#mysql95-oraclelinux9)
-	[`mysql:9.5.0`](#mysql950)
-	[`mysql:9.5.0-oracle`](#mysql950-oracle)
-	[`mysql:9.5.0-oraclelinux9`](#mysql950-oraclelinux9)
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
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:0790c3b4f5f20e4a275575cec26263216b0b3067a1c6a330fe03bd69dedbc3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:a75f25df9a84494dacf5e162dbee5eb655c0b4fc7df9699ab9030a0d6dd04ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232091607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5cad44875910c5fd65acab0a505fe4e9fd7adfa3d81ef1aa247aee539bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b5a1cfaa7c3f4b2e646d7e671f56dd6e02e07b350109f1d2d6fdbc4e9138c`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e8c0b15ba10299b287f32c7cdbbb1061bc53e0d8762b7a3a65ef06827d8fcf`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b3f314407c93cbb0cf3eb5cd7ae2f3b6521e49265f1a91f3e3a63a4682db7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 6.2 MB (6172987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8858a941764948d34cda3ca1462f82bc8420bd9ea624ae6399f71abf74c16a13`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437fb4aadf07d323a5503d8cdb3ccfba33c3c719f7caa56390850db991b43c7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b698ac9d8e790b81d9722f9600c855b9b33fa0f3e5633b34802275ad7e6ea4`  
		Last Modified: Wed, 24 Dec 2025 06:12:57 GMT  
		Size: 49.9 MB (49919226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b58084586a4ef71192b34f01f0ee922c60030cad4aead508e3101252bf2bc`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c53729d27cfd8e1cf8011462dc861683ac60c13681a58668e776054132a038`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 127.9 MB (127886490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e28bac25c5b063df112a248e3d6d43fe1c4d14c924072d492973d41bc0205`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f96bad22960aa13dd29791ccbcac3b60ff5daaa05ce0d9926b77f7c1186a6`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:43c986f1358e6a43da80666c9dbd70398bfb95e65acd80ce8f8e7a640c1f1534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603d046b87e8b3ad2000a4eab362ededf595e1dde7b4d11ee827fab6170e889a`

```dockerfile
```

-	Layers:
	-	`sha256:1f4a7e60dc4183cb340606f97fb738185ba3a4c3cab7e009587dc08e3b3e9fe3`  
		Last Modified: Wed, 24 Dec 2025 10:02:35 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057be4099f5a171d94ab7fb30531decb72e0924949dc021d8eb83821fb5a8dd4`  
		Last Modified: Wed, 24 Dec 2025 10:02:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:937cf083bc193c09c1fa74bf34bb770af9af722d37080fc960db17b1f83e2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227703634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9cf1fc05a33301f71d5c6b146e8057ad995db0ca3dac9e94f9844d4c418d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9392e6dba8fc92a5d056a974c1fae690ce2982f7f75b1362b23467993a08ab`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503c5442fe894220749b303877bc84efdd6da999ff4d8018baf00a0c89813332`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8cd469dff18562801aee3c0f707eb87a3abe51a104b79bf60c05c320002a33`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.8 MB (5799325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3ea63af0df6413cb5d94245a98e0050761afb626446f7c1edf795a7a81f1a2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae42e1c99ab45d04593a61199a4802113d99f72a0c49b7409a8c3d64af26db`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaecbb9c67576b29a25241901d2f7c1e2253f79391d13785f8bffd219688b50a`  
		Last Modified: Wed, 24 Dec 2025 06:13:22 GMT  
		Size: 48.8 MB (48782121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394088591e5cf12d494a7c024be79e67bef0a25117cac828595ee83ca5f5f619`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497e78b904cab04370fcf5ed94d3a2f99c32da3478da9781ad478457f9b8f670`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 126.5 MB (126472072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c728fe9f93d2831a88021c1c763f63030d971eaa90a362b73577d0fab068e`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5dd8caf1882803fa48448eb64f0dda1494326aa52ad90b87435c75d4a97fbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:92c78b49f94706a8788f2b6f293182c701b2cb24c069ace36b83656d685eae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ee4777ce75e06e535f5696b1e3db9e12ef9816a62a37b3586b206604417260`

```dockerfile
```

-	Layers:
	-	`sha256:302b8294bfeee65d850049e570508076bfa0593cc235236ec5ce6288a8b35b4d`  
		Last Modified: Wed, 24 Dec 2025 07:42:34 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6bbb129b7f583f07b1273d7d37427b0c60519c5c53102ca864e713b7bfa234`  
		Last Modified: Wed, 24 Dec 2025 07:42:30 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:bb21c581c0137432cd1553b8a1fe314525828eb04c70be1c77f37e3a2542091c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:197b23ed49671e0fdfe7182dc178442c0244212e571c615b2670f0fba76b1000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183451228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc51e29a81bfcb39cb9123288f3d53297caad10e5ff50f86b1e9fc25d9167ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Dec 2025 23:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:11:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:11:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Mon, 08 Dec 2025 23:11:17 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Dec 2025 23:11:27 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Dec 2025 23:11:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ca305470c24078f730804ba2717ca2ec205faf2cc25eb9962d227034b0db6`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f464afc6a12256c4e176e6f90ea0d98019b1f04087bb25842c7b65940e2c8`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 4.4 MB (4423015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70320fadb8cce9e9ec2ef183fc9fc33a5dacc4106e1d30bb548e1976612d54`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.2 MB (1248663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851bea5201310552fc2d3c3915ff32cf86f3b3a17fd1754f1c2943ab9c5e39`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51934928e1081d7f3a1bad0b7642ebe66681b0b9eb383a4f2517c71b1363d40e`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 15.3 MB (15294776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae55e12c89760c9e781afa0175e6981af72f3298f0499d268d0300d56e88371`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c77c1eda25c220ebba8ef69ebb19dc144003b81378af111d9bea146bd661c`  
		Last Modified: Mon, 08 Dec 2025 23:20:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff96cda79ebb6c40a59bba27504e5246209110a9204e6598381e9389bc6f39`  
		Last Modified: Mon, 08 Dec 2025 23:12:18 GMT  
		Size: 134.2 MB (134245546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff28a1d6b33725512253d32af405815c218ce9d3ddfb379d7ad89d2230797`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df777ec00532bd8890291d610989114861559fef75cb4212bd5524761104f3c`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b779b3847de38f678cbff7625f6ff6bd5675ad0be737397f7534db6b9353eb`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8a051442cf40a48ad634d7c291dfbfe5ff80cf826c20d01b5d9706a21c97cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e185d0af9567d1ea837ad475a7c7df5660cf7efcf05180b5fbc26a777b998f`

```dockerfile
```

-	Layers:
	-	`sha256:341d347ad0353e0ecfa0e2acba668eb46004ce1d084edb9b88c89c796af4dbb9`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fc89ab1938c5c68985223ce9bc70e3f17a51f3e27efc3484951fc76f1e095a`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:bb21c581c0137432cd1553b8a1fe314525828eb04c70be1c77f37e3a2542091c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:197b23ed49671e0fdfe7182dc178442c0244212e571c615b2670f0fba76b1000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183451228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc51e29a81bfcb39cb9123288f3d53297caad10e5ff50f86b1e9fc25d9167ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Dec 2025 23:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:11:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:11:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Mon, 08 Dec 2025 23:11:17 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Dec 2025 23:11:27 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Dec 2025 23:11:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ca305470c24078f730804ba2717ca2ec205faf2cc25eb9962d227034b0db6`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f464afc6a12256c4e176e6f90ea0d98019b1f04087bb25842c7b65940e2c8`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 4.4 MB (4423015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70320fadb8cce9e9ec2ef183fc9fc33a5dacc4106e1d30bb548e1976612d54`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.2 MB (1248663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851bea5201310552fc2d3c3915ff32cf86f3b3a17fd1754f1c2943ab9c5e39`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51934928e1081d7f3a1bad0b7642ebe66681b0b9eb383a4f2517c71b1363d40e`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 15.3 MB (15294776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae55e12c89760c9e781afa0175e6981af72f3298f0499d268d0300d56e88371`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c77c1eda25c220ebba8ef69ebb19dc144003b81378af111d9bea146bd661c`  
		Last Modified: Mon, 08 Dec 2025 23:20:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff96cda79ebb6c40a59bba27504e5246209110a9204e6598381e9389bc6f39`  
		Last Modified: Mon, 08 Dec 2025 23:12:18 GMT  
		Size: 134.2 MB (134245546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff28a1d6b33725512253d32af405815c218ce9d3ddfb379d7ad89d2230797`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df777ec00532bd8890291d610989114861559fef75cb4212bd5524761104f3c`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b779b3847de38f678cbff7625f6ff6bd5675ad0be737397f7534db6b9353eb`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8a051442cf40a48ad634d7c291dfbfe5ff80cf826c20d01b5d9706a21c97cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e185d0af9567d1ea837ad475a7c7df5660cf7efcf05180b5fbc26a777b998f`

```dockerfile
```

-	Layers:
	-	`sha256:341d347ad0353e0ecfa0e2acba668eb46004ce1d084edb9b88c89c796af4dbb9`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fc89ab1938c5c68985223ce9bc70e3f17a51f3e27efc3484951fc76f1e095a`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:0790c3b4f5f20e4a275575cec26263216b0b3067a1c6a330fe03bd69dedbc3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a75f25df9a84494dacf5e162dbee5eb655c0b4fc7df9699ab9030a0d6dd04ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232091607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5cad44875910c5fd65acab0a505fe4e9fd7adfa3d81ef1aa247aee539bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b5a1cfaa7c3f4b2e646d7e671f56dd6e02e07b350109f1d2d6fdbc4e9138c`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e8c0b15ba10299b287f32c7cdbbb1061bc53e0d8762b7a3a65ef06827d8fcf`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b3f314407c93cbb0cf3eb5cd7ae2f3b6521e49265f1a91f3e3a63a4682db7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 6.2 MB (6172987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8858a941764948d34cda3ca1462f82bc8420bd9ea624ae6399f71abf74c16a13`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437fb4aadf07d323a5503d8cdb3ccfba33c3c719f7caa56390850db991b43c7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b698ac9d8e790b81d9722f9600c855b9b33fa0f3e5633b34802275ad7e6ea4`  
		Last Modified: Wed, 24 Dec 2025 06:12:57 GMT  
		Size: 49.9 MB (49919226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b58084586a4ef71192b34f01f0ee922c60030cad4aead508e3101252bf2bc`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c53729d27cfd8e1cf8011462dc861683ac60c13681a58668e776054132a038`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 127.9 MB (127886490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e28bac25c5b063df112a248e3d6d43fe1c4d14c924072d492973d41bc0205`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f96bad22960aa13dd29791ccbcac3b60ff5daaa05ce0d9926b77f7c1186a6`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:43c986f1358e6a43da80666c9dbd70398bfb95e65acd80ce8f8e7a640c1f1534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603d046b87e8b3ad2000a4eab362ededf595e1dde7b4d11ee827fab6170e889a`

```dockerfile
```

-	Layers:
	-	`sha256:1f4a7e60dc4183cb340606f97fb738185ba3a4c3cab7e009587dc08e3b3e9fe3`  
		Last Modified: Wed, 24 Dec 2025 10:02:35 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057be4099f5a171d94ab7fb30531decb72e0924949dc021d8eb83821fb5a8dd4`  
		Last Modified: Wed, 24 Dec 2025 10:02:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:937cf083bc193c09c1fa74bf34bb770af9af722d37080fc960db17b1f83e2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227703634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9cf1fc05a33301f71d5c6b146e8057ad995db0ca3dac9e94f9844d4c418d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9392e6dba8fc92a5d056a974c1fae690ce2982f7f75b1362b23467993a08ab`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503c5442fe894220749b303877bc84efdd6da999ff4d8018baf00a0c89813332`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8cd469dff18562801aee3c0f707eb87a3abe51a104b79bf60c05c320002a33`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.8 MB (5799325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3ea63af0df6413cb5d94245a98e0050761afb626446f7c1edf795a7a81f1a2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae42e1c99ab45d04593a61199a4802113d99f72a0c49b7409a8c3d64af26db`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaecbb9c67576b29a25241901d2f7c1e2253f79391d13785f8bffd219688b50a`  
		Last Modified: Wed, 24 Dec 2025 06:13:22 GMT  
		Size: 48.8 MB (48782121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394088591e5cf12d494a7c024be79e67bef0a25117cac828595ee83ca5f5f619`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497e78b904cab04370fcf5ed94d3a2f99c32da3478da9781ad478457f9b8f670`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 126.5 MB (126472072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c728fe9f93d2831a88021c1c763f63030d971eaa90a362b73577d0fab068e`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5dd8caf1882803fa48448eb64f0dda1494326aa52ad90b87435c75d4a97fbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92c78b49f94706a8788f2b6f293182c701b2cb24c069ace36b83656d685eae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ee4777ce75e06e535f5696b1e3db9e12ef9816a62a37b3586b206604417260`

```dockerfile
```

-	Layers:
	-	`sha256:302b8294bfeee65d850049e570508076bfa0593cc235236ec5ce6288a8b35b4d`  
		Last Modified: Wed, 24 Dec 2025 07:42:34 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6bbb129b7f583f07b1273d7d37427b0c60519c5c53102ca864e713b7bfa234`  
		Last Modified: Wed, 24 Dec 2025 07:42:30 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:0790c3b4f5f20e4a275575cec26263216b0b3067a1c6a330fe03bd69dedbc3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a75f25df9a84494dacf5e162dbee5eb655c0b4fc7df9699ab9030a0d6dd04ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232091607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5cad44875910c5fd65acab0a505fe4e9fd7adfa3d81ef1aa247aee539bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b5a1cfaa7c3f4b2e646d7e671f56dd6e02e07b350109f1d2d6fdbc4e9138c`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e8c0b15ba10299b287f32c7cdbbb1061bc53e0d8762b7a3a65ef06827d8fcf`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b3f314407c93cbb0cf3eb5cd7ae2f3b6521e49265f1a91f3e3a63a4682db7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 6.2 MB (6172987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8858a941764948d34cda3ca1462f82bc8420bd9ea624ae6399f71abf74c16a13`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437fb4aadf07d323a5503d8cdb3ccfba33c3c719f7caa56390850db991b43c7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b698ac9d8e790b81d9722f9600c855b9b33fa0f3e5633b34802275ad7e6ea4`  
		Last Modified: Wed, 24 Dec 2025 06:12:57 GMT  
		Size: 49.9 MB (49919226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b58084586a4ef71192b34f01f0ee922c60030cad4aead508e3101252bf2bc`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c53729d27cfd8e1cf8011462dc861683ac60c13681a58668e776054132a038`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 127.9 MB (127886490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e28bac25c5b063df112a248e3d6d43fe1c4d14c924072d492973d41bc0205`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f96bad22960aa13dd29791ccbcac3b60ff5daaa05ce0d9926b77f7c1186a6`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:43c986f1358e6a43da80666c9dbd70398bfb95e65acd80ce8f8e7a640c1f1534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603d046b87e8b3ad2000a4eab362ededf595e1dde7b4d11ee827fab6170e889a`

```dockerfile
```

-	Layers:
	-	`sha256:1f4a7e60dc4183cb340606f97fb738185ba3a4c3cab7e009587dc08e3b3e9fe3`  
		Last Modified: Wed, 24 Dec 2025 10:02:35 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057be4099f5a171d94ab7fb30531decb72e0924949dc021d8eb83821fb5a8dd4`  
		Last Modified: Wed, 24 Dec 2025 10:02:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:937cf083bc193c09c1fa74bf34bb770af9af722d37080fc960db17b1f83e2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227703634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9cf1fc05a33301f71d5c6b146e8057ad995db0ca3dac9e94f9844d4c418d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9392e6dba8fc92a5d056a974c1fae690ce2982f7f75b1362b23467993a08ab`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503c5442fe894220749b303877bc84efdd6da999ff4d8018baf00a0c89813332`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8cd469dff18562801aee3c0f707eb87a3abe51a104b79bf60c05c320002a33`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.8 MB (5799325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3ea63af0df6413cb5d94245a98e0050761afb626446f7c1edf795a7a81f1a2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae42e1c99ab45d04593a61199a4802113d99f72a0c49b7409a8c3d64af26db`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaecbb9c67576b29a25241901d2f7c1e2253f79391d13785f8bffd219688b50a`  
		Last Modified: Wed, 24 Dec 2025 06:13:22 GMT  
		Size: 48.8 MB (48782121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394088591e5cf12d494a7c024be79e67bef0a25117cac828595ee83ca5f5f619`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497e78b904cab04370fcf5ed94d3a2f99c32da3478da9781ad478457f9b8f670`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 126.5 MB (126472072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c728fe9f93d2831a88021c1c763f63030d971eaa90a362b73577d0fab068e`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5dd8caf1882803fa48448eb64f0dda1494326aa52ad90b87435c75d4a97fbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92c78b49f94706a8788f2b6f293182c701b2cb24c069ace36b83656d685eae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ee4777ce75e06e535f5696b1e3db9e12ef9816a62a37b3586b206604417260`

```dockerfile
```

-	Layers:
	-	`sha256:302b8294bfeee65d850049e570508076bfa0593cc235236ec5ce6288a8b35b4d`  
		Last Modified: Wed, 24 Dec 2025 07:42:34 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6bbb129b7f583f07b1273d7d37427b0c60519c5c53102ca864e713b7bfa234`  
		Last Modified: Wed, 24 Dec 2025 07:42:30 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44`

```console
$ docker pull mysql@sha256:0790c3b4f5f20e4a275575cec26263216b0b3067a1c6a330fe03bd69dedbc3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44` - linux; amd64

```console
$ docker pull mysql@sha256:a75f25df9a84494dacf5e162dbee5eb655c0b4fc7df9699ab9030a0d6dd04ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232091607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5cad44875910c5fd65acab0a505fe4e9fd7adfa3d81ef1aa247aee539bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b5a1cfaa7c3f4b2e646d7e671f56dd6e02e07b350109f1d2d6fdbc4e9138c`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e8c0b15ba10299b287f32c7cdbbb1061bc53e0d8762b7a3a65ef06827d8fcf`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b3f314407c93cbb0cf3eb5cd7ae2f3b6521e49265f1a91f3e3a63a4682db7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 6.2 MB (6172987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8858a941764948d34cda3ca1462f82bc8420bd9ea624ae6399f71abf74c16a13`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437fb4aadf07d323a5503d8cdb3ccfba33c3c719f7caa56390850db991b43c7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b698ac9d8e790b81d9722f9600c855b9b33fa0f3e5633b34802275ad7e6ea4`  
		Last Modified: Wed, 24 Dec 2025 06:12:57 GMT  
		Size: 49.9 MB (49919226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b58084586a4ef71192b34f01f0ee922c60030cad4aead508e3101252bf2bc`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c53729d27cfd8e1cf8011462dc861683ac60c13681a58668e776054132a038`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 127.9 MB (127886490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e28bac25c5b063df112a248e3d6d43fe1c4d14c924072d492973d41bc0205`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f96bad22960aa13dd29791ccbcac3b60ff5daaa05ce0d9926b77f7c1186a6`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:43c986f1358e6a43da80666c9dbd70398bfb95e65acd80ce8f8e7a640c1f1534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603d046b87e8b3ad2000a4eab362ededf595e1dde7b4d11ee827fab6170e889a`

```dockerfile
```

-	Layers:
	-	`sha256:1f4a7e60dc4183cb340606f97fb738185ba3a4c3cab7e009587dc08e3b3e9fe3`  
		Last Modified: Wed, 24 Dec 2025 10:02:35 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057be4099f5a171d94ab7fb30531decb72e0924949dc021d8eb83821fb5a8dd4`  
		Last Modified: Wed, 24 Dec 2025 10:02:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:937cf083bc193c09c1fa74bf34bb770af9af722d37080fc960db17b1f83e2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227703634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9cf1fc05a33301f71d5c6b146e8057ad995db0ca3dac9e94f9844d4c418d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9392e6dba8fc92a5d056a974c1fae690ce2982f7f75b1362b23467993a08ab`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503c5442fe894220749b303877bc84efdd6da999ff4d8018baf00a0c89813332`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8cd469dff18562801aee3c0f707eb87a3abe51a104b79bf60c05c320002a33`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.8 MB (5799325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3ea63af0df6413cb5d94245a98e0050761afb626446f7c1edf795a7a81f1a2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae42e1c99ab45d04593a61199a4802113d99f72a0c49b7409a8c3d64af26db`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaecbb9c67576b29a25241901d2f7c1e2253f79391d13785f8bffd219688b50a`  
		Last Modified: Wed, 24 Dec 2025 06:13:22 GMT  
		Size: 48.8 MB (48782121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394088591e5cf12d494a7c024be79e67bef0a25117cac828595ee83ca5f5f619`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497e78b904cab04370fcf5ed94d3a2f99c32da3478da9781ad478457f9b8f670`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 126.5 MB (126472072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c728fe9f93d2831a88021c1c763f63030d971eaa90a362b73577d0fab068e`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5dd8caf1882803fa48448eb64f0dda1494326aa52ad90b87435c75d4a97fbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:92c78b49f94706a8788f2b6f293182c701b2cb24c069ace36b83656d685eae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ee4777ce75e06e535f5696b1e3db9e12ef9816a62a37b3586b206604417260`

```dockerfile
```

-	Layers:
	-	`sha256:302b8294bfeee65d850049e570508076bfa0593cc235236ec5ce6288a8b35b4d`  
		Last Modified: Wed, 24 Dec 2025 07:42:34 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6bbb129b7f583f07b1273d7d37427b0c60519c5c53102ca864e713b7bfa234`  
		Last Modified: Wed, 24 Dec 2025 07:42:30 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-bookworm`

```console
$ docker pull mysql@sha256:bb21c581c0137432cd1553b8a1fe314525828eb04c70be1c77f37e3a2542091c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:197b23ed49671e0fdfe7182dc178442c0244212e571c615b2670f0fba76b1000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183451228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc51e29a81bfcb39cb9123288f3d53297caad10e5ff50f86b1e9fc25d9167ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Dec 2025 23:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:11:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:11:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Mon, 08 Dec 2025 23:11:17 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Dec 2025 23:11:27 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Dec 2025 23:11:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ca305470c24078f730804ba2717ca2ec205faf2cc25eb9962d227034b0db6`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f464afc6a12256c4e176e6f90ea0d98019b1f04087bb25842c7b65940e2c8`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 4.4 MB (4423015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70320fadb8cce9e9ec2ef183fc9fc33a5dacc4106e1d30bb548e1976612d54`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.2 MB (1248663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851bea5201310552fc2d3c3915ff32cf86f3b3a17fd1754f1c2943ab9c5e39`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51934928e1081d7f3a1bad0b7642ebe66681b0b9eb383a4f2517c71b1363d40e`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 15.3 MB (15294776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae55e12c89760c9e781afa0175e6981af72f3298f0499d268d0300d56e88371`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c77c1eda25c220ebba8ef69ebb19dc144003b81378af111d9bea146bd661c`  
		Last Modified: Mon, 08 Dec 2025 23:20:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff96cda79ebb6c40a59bba27504e5246209110a9204e6598381e9389bc6f39`  
		Last Modified: Mon, 08 Dec 2025 23:12:18 GMT  
		Size: 134.2 MB (134245546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff28a1d6b33725512253d32af405815c218ce9d3ddfb379d7ad89d2230797`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df777ec00532bd8890291d610989114861559fef75cb4212bd5524761104f3c`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b779b3847de38f678cbff7625f6ff6bd5675ad0be737397f7534db6b9353eb`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8a051442cf40a48ad634d7c291dfbfe5ff80cf826c20d01b5d9706a21c97cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e185d0af9567d1ea837ad475a7c7df5660cf7efcf05180b5fbc26a777b998f`

```dockerfile
```

-	Layers:
	-	`sha256:341d347ad0353e0ecfa0e2acba668eb46004ce1d084edb9b88c89c796af4dbb9`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fc89ab1938c5c68985223ce9bc70e3f17a51f3e27efc3484951fc76f1e095a`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-debian`

```console
$ docker pull mysql@sha256:bb21c581c0137432cd1553b8a1fe314525828eb04c70be1c77f37e3a2542091c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-debian` - linux; amd64

```console
$ docker pull mysql@sha256:197b23ed49671e0fdfe7182dc178442c0244212e571c615b2670f0fba76b1000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183451228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc51e29a81bfcb39cb9123288f3d53297caad10e5ff50f86b1e9fc25d9167ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 08 Dec 2025 23:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:11:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:11:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 08 Dec 2025 23:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Mon, 08 Dec 2025 23:11:17 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 08 Dec 2025 23:11:27 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 08 Dec 2025 23:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:27 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 08 Dec 2025 23:11:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ca305470c24078f730804ba2717ca2ec205faf2cc25eb9962d227034b0db6`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f464afc6a12256c4e176e6f90ea0d98019b1f04087bb25842c7b65940e2c8`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 4.4 MB (4423015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c70320fadb8cce9e9ec2ef183fc9fc33a5dacc4106e1d30bb548e1976612d54`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 1.2 MB (1248663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851bea5201310552fc2d3c3915ff32cf86f3b3a17fd1754f1c2943ab9c5e39`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51934928e1081d7f3a1bad0b7642ebe66681b0b9eb383a4f2517c71b1363d40e`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 15.3 MB (15294776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae55e12c89760c9e781afa0175e6981af72f3298f0499d268d0300d56e88371`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c77c1eda25c220ebba8ef69ebb19dc144003b81378af111d9bea146bd661c`  
		Last Modified: Mon, 08 Dec 2025 23:20:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff96cda79ebb6c40a59bba27504e5246209110a9204e6598381e9389bc6f39`  
		Last Modified: Mon, 08 Dec 2025 23:12:18 GMT  
		Size: 134.2 MB (134245546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff28a1d6b33725512253d32af405815c218ce9d3ddfb379d7ad89d2230797`  
		Last Modified: Mon, 08 Dec 2025 23:12:02 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df777ec00532bd8890291d610989114861559fef75cb4212bd5524761104f3c`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b779b3847de38f678cbff7625f6ff6bd5675ad0be737397f7534db6b9353eb`  
		Last Modified: Mon, 08 Dec 2025 23:12:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:4f8a051442cf40a48ad634d7c291dfbfe5ff80cf826c20d01b5d9706a21c97cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e185d0af9567d1ea837ad475a7c7df5660cf7efcf05180b5fbc26a777b998f`

```dockerfile
```

-	Layers:
	-	`sha256:341d347ad0353e0ecfa0e2acba668eb46004ce1d084edb9b88c89c796af4dbb9`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95fc89ab1938c5c68985223ce9bc70e3f17a51f3e27efc3484951fc76f1e095a`  
		Last Modified: Tue, 09 Dec 2025 01:02:50 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oracle`

```console
$ docker pull mysql@sha256:0790c3b4f5f20e4a275575cec26263216b0b3067a1c6a330fe03bd69dedbc3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a75f25df9a84494dacf5e162dbee5eb655c0b4fc7df9699ab9030a0d6dd04ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232091607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5cad44875910c5fd65acab0a505fe4e9fd7adfa3d81ef1aa247aee539bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b5a1cfaa7c3f4b2e646d7e671f56dd6e02e07b350109f1d2d6fdbc4e9138c`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e8c0b15ba10299b287f32c7cdbbb1061bc53e0d8762b7a3a65ef06827d8fcf`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b3f314407c93cbb0cf3eb5cd7ae2f3b6521e49265f1a91f3e3a63a4682db7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 6.2 MB (6172987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8858a941764948d34cda3ca1462f82bc8420bd9ea624ae6399f71abf74c16a13`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437fb4aadf07d323a5503d8cdb3ccfba33c3c719f7caa56390850db991b43c7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b698ac9d8e790b81d9722f9600c855b9b33fa0f3e5633b34802275ad7e6ea4`  
		Last Modified: Wed, 24 Dec 2025 06:12:57 GMT  
		Size: 49.9 MB (49919226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b58084586a4ef71192b34f01f0ee922c60030cad4aead508e3101252bf2bc`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c53729d27cfd8e1cf8011462dc861683ac60c13681a58668e776054132a038`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 127.9 MB (127886490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e28bac25c5b063df112a248e3d6d43fe1c4d14c924072d492973d41bc0205`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f96bad22960aa13dd29791ccbcac3b60ff5daaa05ce0d9926b77f7c1186a6`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:43c986f1358e6a43da80666c9dbd70398bfb95e65acd80ce8f8e7a640c1f1534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603d046b87e8b3ad2000a4eab362ededf595e1dde7b4d11ee827fab6170e889a`

```dockerfile
```

-	Layers:
	-	`sha256:1f4a7e60dc4183cb340606f97fb738185ba3a4c3cab7e009587dc08e3b3e9fe3`  
		Last Modified: Wed, 24 Dec 2025 10:02:35 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057be4099f5a171d94ab7fb30531decb72e0924949dc021d8eb83821fb5a8dd4`  
		Last Modified: Wed, 24 Dec 2025 10:02:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:937cf083bc193c09c1fa74bf34bb770af9af722d37080fc960db17b1f83e2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227703634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9cf1fc05a33301f71d5c6b146e8057ad995db0ca3dac9e94f9844d4c418d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9392e6dba8fc92a5d056a974c1fae690ce2982f7f75b1362b23467993a08ab`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503c5442fe894220749b303877bc84efdd6da999ff4d8018baf00a0c89813332`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8cd469dff18562801aee3c0f707eb87a3abe51a104b79bf60c05c320002a33`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.8 MB (5799325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3ea63af0df6413cb5d94245a98e0050761afb626446f7c1edf795a7a81f1a2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae42e1c99ab45d04593a61199a4802113d99f72a0c49b7409a8c3d64af26db`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaecbb9c67576b29a25241901d2f7c1e2253f79391d13785f8bffd219688b50a`  
		Last Modified: Wed, 24 Dec 2025 06:13:22 GMT  
		Size: 48.8 MB (48782121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394088591e5cf12d494a7c024be79e67bef0a25117cac828595ee83ca5f5f619`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497e78b904cab04370fcf5ed94d3a2f99c32da3478da9781ad478457f9b8f670`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 126.5 MB (126472072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c728fe9f93d2831a88021c1c763f63030d971eaa90a362b73577d0fab068e`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5dd8caf1882803fa48448eb64f0dda1494326aa52ad90b87435c75d4a97fbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:92c78b49f94706a8788f2b6f293182c701b2cb24c069ace36b83656d685eae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ee4777ce75e06e535f5696b1e3db9e12ef9816a62a37b3586b206604417260`

```dockerfile
```

-	Layers:
	-	`sha256:302b8294bfeee65d850049e570508076bfa0593cc235236ec5ce6288a8b35b4d`  
		Last Modified: Wed, 24 Dec 2025 07:42:34 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6bbb129b7f583f07b1273d7d37427b0c60519c5c53102ca864e713b7bfa234`  
		Last Modified: Wed, 24 Dec 2025 07:42:30 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oraclelinux9`

```console
$ docker pull mysql@sha256:0790c3b4f5f20e4a275575cec26263216b0b3067a1c6a330fe03bd69dedbc3e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a75f25df9a84494dacf5e162dbee5eb655c0b4fc7df9699ab9030a0d6dd04ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232091607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf5cad44875910c5fd65acab0a505fe4e9fd7adfa3d81ef1aa247aee539bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:16 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:16 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:12 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b5a1cfaa7c3f4b2e646d7e671f56dd6e02e07b350109f1d2d6fdbc4e9138c`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e8c0b15ba10299b287f32c7cdbbb1061bc53e0d8762b7a3a65ef06827d8fcf`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b3f314407c93cbb0cf3eb5cd7ae2f3b6521e49265f1a91f3e3a63a4682db7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 6.2 MB (6172987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8858a941764948d34cda3ca1462f82bc8420bd9ea624ae6399f71abf74c16a13`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2437fb4aadf07d323a5503d8cdb3ccfba33c3c719f7caa56390850db991b43c7`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b698ac9d8e790b81d9722f9600c855b9b33fa0f3e5633b34802275ad7e6ea4`  
		Last Modified: Wed, 24 Dec 2025 06:12:57 GMT  
		Size: 49.9 MB (49919226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b58084586a4ef71192b34f01f0ee922c60030cad4aead508e3101252bf2bc`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c53729d27cfd8e1cf8011462dc861683ac60c13681a58668e776054132a038`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 127.9 MB (127886490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e28bac25c5b063df112a248e3d6d43fe1c4d14c924072d492973d41bc0205`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f96bad22960aa13dd29791ccbcac3b60ff5daaa05ce0d9926b77f7c1186a6`  
		Last Modified: Wed, 24 Dec 2025 06:12:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:43c986f1358e6a43da80666c9dbd70398bfb95e65acd80ce8f8e7a640c1f1534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603d046b87e8b3ad2000a4eab362ededf595e1dde7b4d11ee827fab6170e889a`

```dockerfile
```

-	Layers:
	-	`sha256:1f4a7e60dc4183cb340606f97fb738185ba3a4c3cab7e009587dc08e3b3e9fe3`  
		Last Modified: Wed, 24 Dec 2025 10:02:35 GMT  
		Size: 14.6 MB (14620429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057be4099f5a171d94ab7fb30531decb72e0924949dc021d8eb83821fb5a8dd4`  
		Last Modified: Wed, 24 Dec 2025 10:02:36 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:937cf083bc193c09c1fa74bf34bb770af9af722d37080fc960db17b1f83e2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227703634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad9cf1fc05a33301f71d5c6b146e8057ad995db0ca3dac9e94f9844d4c418d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:58 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 24 Dec 2025 06:11:25 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:11:25 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:53 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Wed, 24 Dec 2025 06:12:28 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 24 Dec 2025 06:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:29 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9392e6dba8fc92a5d056a974c1fae690ce2982f7f75b1362b23467993a08ab`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503c5442fe894220749b303877bc84efdd6da999ff4d8018baf00a0c89813332`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8cd469dff18562801aee3c0f707eb87a3abe51a104b79bf60c05c320002a33`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.8 MB (5799325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3ea63af0df6413cb5d94245a98e0050761afb626446f7c1edf795a7a81f1a2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fae42e1c99ab45d04593a61199a4802113d99f72a0c49b7409a8c3d64af26db`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaecbb9c67576b29a25241901d2f7c1e2253f79391d13785f8bffd219688b50a`  
		Last Modified: Wed, 24 Dec 2025 06:13:22 GMT  
		Size: 48.8 MB (48782121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394088591e5cf12d494a7c024be79e67bef0a25117cac828595ee83ca5f5f619`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497e78b904cab04370fcf5ed94d3a2f99c32da3478da9781ad478457f9b8f670`  
		Last Modified: Wed, 24 Dec 2025 06:13:14 GMT  
		Size: 126.5 MB (126472072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c728fe9f93d2831a88021c1c763f63030d971eaa90a362b73577d0fab068e`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5dd8caf1882803fa48448eb64f0dda1494326aa52ad90b87435c75d4a97fbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:92c78b49f94706a8788f2b6f293182c701b2cb24c069ace36b83656d685eae12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ee4777ce75e06e535f5696b1e3db9e12ef9816a62a37b3586b206604417260`

```dockerfile
```

-	Layers:
	-	`sha256:302b8294bfeee65d850049e570508076bfa0593cc235236ec5ce6288a8b35b4d`  
		Last Modified: Wed, 24 Dec 2025 07:42:34 GMT  
		Size: 14.6 MB (14618777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6bbb129b7f583f07b1273d7d37427b0c60519c5c53102ca864e713b7bfa234`  
		Last Modified: Wed, 24 Dec 2025 07:42:30 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oracle`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oraclelinux9`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oracle`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oraclelinux9`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oracle`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oraclelinux9`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:1f5b0aca09cfa06d9a7b89b28d349c1e01ba0d31339a4786fbcb3d5927070130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:eaf64e87ae0d1136d46405ad56c9010de509fd5b949b9c8ede45c94f47804d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233029875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3dcc4ab5604ab9bdf1054833d4f0ac396465de830ccac42d4f59131db9ba23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:31 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:55 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f09f84111f93fbe8a1859f5d8ab6e696712521d2b766cc3b3b5df484bcbc`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cff4cd5a8c6372d6b44b827071d111467bf7b56fc3d4d6ecb25100fe8dd52`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5e042ddb8cbeeca2391384c1f9f2d156829fe54036f5c410f8253c941744b`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8dd19eb384d86bb1ff0a95a3aecd579d3e851b1a26968c6bb6f1391c5ef9b5`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d1b4085ee54a6975bf3f76b557ded2b67b33215920d76d4fef88fa7fe74b6`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0c90f9a39fae0e14a8269a6c55236066fff18184b2a22e526c18193c1c8bf`  
		Last Modified: Wed, 24 Dec 2025 06:13:04 GMT  
		Size: 47.8 MB (47809406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a353cf71214322d0e570c14ac635e15f3703a46319253f2b6420db48b8b476`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866beeda62191b2eef3ee95e0532bd4a10fc4a87b9fc693ad97519b3cef6008`  
		Last Modified: Wed, 24 Dec 2025 06:14:06 GMT  
		Size: 130.9 MB (130934777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac6a049cbaed70d12c4b99bcb45731bb956ad29555f48b6a499ea26bed1d37`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aa5cde8fbee0dc960a5be57a3d0e6897a50f7f78e21ddd6cef3bb8c1cc95a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ebf5d22bda7244334b2b886d612e587565cbdd554b7ddbd90cae8f0529311`

```dockerfile
```

-	Layers:
	-	`sha256:c9fec2869c6e4656095143f7f34037168cfc390a3f214bec46fae40c7e6102a1`  
		Last Modified: Wed, 24 Dec 2025 10:02:22 GMT  
		Size: 14.9 MB (14897250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff0d1488e4ec2dc3b768c8b3c8111ad9a6d2f5bf5c9efdf184e9bba665e732b`  
		Last Modified: Wed, 24 Dec 2025 10:02:21 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1f7bcc673aebdb50da0a64f6b51d81c2a4c9535113b6527755b26346222bda7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1219071f5f1819494488d45fe80053e31d90a77835dca6ff40f18db9cd0641ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:52 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:55 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 24 Dec 2025 06:11:22 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:11:22 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:52 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Wed, 24 Dec 2025 06:12:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef57b7cb7c563a4d7b1ba3f6c2c18eab27db16cdb8bc8a6b399b8c537e4421`  
		Last Modified: Wed, 24 Dec 2025 06:13:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a20461de0fce1e427684555b2e90b2f8f0b1d21558b4069870f3ef3817af639`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23850e829fa994e3c16d4ac8a6ff2c39bbdac87a8f38daed68e501f419ebfb`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.8 MB (5799290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcfb096d49ba09a1a7a534224951207319baa4081de415c4ad875910321ec4`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61e4682d2223b1d1dcc144a8ef8c0bbf874af4a456c096ec3fd6f522e6f4b2`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2a7a543ec555d31e409c463c025ec81cec2314ff48dadb2b2eb4d65723cff`  
		Last Modified: Wed, 24 Dec 2025 06:13:19 GMT  
		Size: 46.7 MB (46689785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c107e3f09284e1dd75d5a3b4151e36297c94ae5c23b6861842c89988abb0cb`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eed4f5fd7589365b2ec9181ff5286d120721aaa361ed93bbb1c2b502fe5eb9`  
		Last Modified: Wed, 24 Dec 2025 06:14:11 GMT  
		Size: 129.3 MB (129331490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e9e6191405a6484284d5df832eb871061fd305fa5774bcdd3c03abfb73d4d`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:0f586ae41d7bb0ad1693aa30ac8a432969aa4bdd08e11a779a9153ba4d67c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c09df8659b17ce4bf5b5e93a54821099f37ba888c981743368d3afd15d047`

```dockerfile
```

-	Layers:
	-	`sha256:599eb1cbbbfc311e2d7a78f75c9413f251d007381e94e3830976fad7dad1679e`  
		Last Modified: Wed, 24 Dec 2025 09:20:40 GMT  
		Size: 14.9 MB (14895670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd18baa6d821c897eb06d13f4002e4c35181a061c578965e138b1c99f464a532`  
		Last Modified: Wed, 24 Dec 2025 09:20:27 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:5ca0a273ed28c73acaef91da8bf1eca3711bee94bce4c378d42846375e645a72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:63cfc76dd50bc5da75cc4cc758ef1c396ea5c7df07065240c593ce3783b53b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274743760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43463387c19a19c69fd00f32d492cb747cf738c30ef0628664280f49a3f4f55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:11:06 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:11:07 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:07 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:34 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:12:11 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:12:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:12:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:12:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:12:12 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:12:12 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fdee9efbea5e86e637e429fc5305ba659433ef540a929bd56bd86aa3358b1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739ccce10fef39d33dc6bb0eb200524c4d79475f2755547c44be0e53d691b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ade15623158f018e163bf9f1e90eb96de7a4eb6e528ba2883c3036d9e2bb88`  
		Last Modified: Wed, 24 Dec 2025 06:13:02 GMT  
		Size: 6.2 MB (6172933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494a5617c302b456243d415c53fe84ca25c3002ce56258e577cfbc3cf0030`  
		Last Modified: Wed, 24 Dec 2025 06:13:07 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977bb8125788e8bc0f7fe950bb54ef5cfe7af769b56a060959f67e5c35b5d26`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94829adeb7d577cc316253253ea4f4743a36d91e5e4eb9e62cdf5a4010350d6d`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 51.3 MB (51339376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33d02f9e9dd93519837963c518dfe0f1a06e23a48b54ee7305af65f9aec0df`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc357b5ee6d221661a87283a9d5ef70812046bf6c430755a5f876cb2c04d6a2a`  
		Last Modified: Wed, 24 Dec 2025 06:13:27 GMT  
		Size: 169.1 MB (169118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9dbd900b6d31b0f791ac15f95720064ddd084b130d6acd6d2201f5e5c0dd1`  
		Last Modified: Wed, 24 Dec 2025 06:13:01 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5ed4dc7ecf7cc5cd98ec23cee55c866fe8e132c4de54c25fb7e52a5043301fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764317e87c39aafee8b7f55b056352f3652bd0e2179fc24a4b6016e49c03b73a`

```dockerfile
```

-	Layers:
	-	`sha256:4fdb571547772cf1740c1332b92f27bcbfa9ac263e87d62c99a67e967fea62f3`  
		Last Modified: Wed, 24 Dec 2025 10:03:11 GMT  
		Size: 17.8 MB (17811684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64911a6c79e2708a3d0d05552812d1b887bcebf22ca6b7522c14f67c77c7e98a`  
		Last Modified: Wed, 24 Dec 2025 10:03:21 GMT  
		Size: 35.3 KB (35273 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:680dc1e3ad62053eaf4a462be20f2477be4f6591e3f14a92c6c54f818bd2e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269809702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c3266b6b77f63a9064496565abe1d16fd04705b1343257bd112f2ba43b993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:10:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 24 Dec 2025 06:10:16 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Dec 2025 06:10:16 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Dec 2025 06:10:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 24 Dec 2025 06:10:42 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:10:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 24 Dec 2025 06:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 24 Dec 2025 06:11:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Wed, 24 Dec 2025 06:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 24 Dec 2025 06:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 06:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 06:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 24 Dec 2025 06:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fd8b6499592fd29b866d82e00c902dc0cf011626b9e4d7c5b359337c9d5c2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a69bbc706bc44e212923825ae863066d80f00788c91a7e8b71062005e6ecf2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 737.5 KB (737531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e82b6f8b9ae03ce4ee03088d040b7bfad2a74bf0ff7fb6b1e068b54ebb8e2`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 5.8 MB (5799305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7841c3476196b92477b0dd4ca4c0eef34e2479e14be94f513d6d7b1e606de99`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e5be81314066f565ac92b06f6ae72fbb0a9822deb7c687a60061eb1fd5324`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54d7164805c698578999f62b9235542d8ebfe400b865080c1df43651161f23`  
		Last Modified: Wed, 24 Dec 2025 06:12:42 GMT  
		Size: 50.0 MB (49963256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508c5e2469fb3678807c0c60746f538dba179d8e0605b09a20b4303cb7b5e3a`  
		Last Modified: Wed, 24 Dec 2025 06:12:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31529acca3c94289a71c7f6fb2a7da7cf211cb86a0ee0fc26d9aa21ae97035`  
		Last Modified: Wed, 24 Dec 2025 07:13:56 GMT  
		Size: 167.4 MB (167397125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea9e2fa7b259a7f696c6b504bf2e25d81be3b389761ac76a356902dbb092322`  
		Last Modified: Wed, 24 Dec 2025 06:12:44 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fe7ebea6123c82aa390e8830f44dfe337bc3839dadb3e038bc8c9f5d5d817ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd9b380ac05c6ec1a40edae73b4008071c2daa78804d0d8f0dc98ea680643`

```dockerfile
```

-	Layers:
	-	`sha256:29a176dedfcc07d16a5456839c883bbc0fa2ce727dd9a42009c02f22590701dc`  
		Last Modified: Wed, 24 Dec 2025 10:03:35 GMT  
		Size: 17.8 MB (17806823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd08d119f921e48f76173ea46938b5eb831a5be1bb60e444f688565113b7b2`  
		Last Modified: Wed, 24 Dec 2025 10:03:36 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
