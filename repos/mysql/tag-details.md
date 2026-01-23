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
-	[`mysql:8.0.45`](#mysql8045)
-	[`mysql:8.0.45-bookworm`](#mysql8045-bookworm)
-	[`mysql:8.0.45-debian`](#mysql8045-debian)
-	[`mysql:8.0.45-oracle`](#mysql8045-oracle)
-	[`mysql:8.0.45-oraclelinux9`](#mysql8045-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.8`](#mysql848)
-	[`mysql:8.4.8-oracle`](#mysql848-oracle)
-	[`mysql:8.4.8-oraclelinux9`](#mysql848-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.6`](#mysql96)
-	[`mysql:9.6-oracle`](#mysql96-oracle)
-	[`mysql:9.6-oraclelinux9`](#mysql96-oraclelinux9)
-	[`mysql:9.6.0`](#mysql960)
-	[`mysql:9.6.0-oracle`](#mysql960-oracle)
-	[`mysql:9.6.0-oraclelinux9`](#mysql960-oraclelinux9)
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
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:7a9d63525e8072408862dd62226440db869e745e37f36968b26e3ef03d6e9641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:5aa923a8d649f78968c4db36a83f7173f56d2267742e2f66b7943a08082df623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc31df46db658500d1d56d2037d3b6e564b69de61596b8fcd2ca1be2c9c989b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:05:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:06:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:06:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:06:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9c9ba7072382f7daa02eb7b0d2e620fd996e84a7e2c3f478157c656a4c2615`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be113d11b355d3d5d8ffd0f14b7b2ed4aa30885451c737fe0dc3f8393a69e044`  
		Last Modified: Fri, 23 Jan 2026 01:06:36 GMT  
		Size: 49.9 MB (49923216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bdba0501248e4b8e12eec72b73448109aa526562320546fa27ade027fa72b3`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a2bfb30cdf133ff644108f6f7e6dda508805c52e6c3de2ae396bc9e9f26987`  
		Last Modified: Fri, 23 Jan 2026 01:06:37 GMT  
		Size: 128.1 MB (128104088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ed66656b21312cedae686fa2aaae9f891330d146241e231e45b4a726d9df4a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0ceff8a81bb18f2dfd90b4e468e7d7128cac1376502e996fd4303d924a063a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f51dcb25eecfb1cee34d26e4a601778904eca1835d107a2607a15f629965b36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ac841b89f7909db5fa022b4ec199aada79e7ce4f5c20c060c82b51229488d`

```dockerfile
```

-	Layers:
	-	`sha256:e032523bbbc99c9df18c189f34a21d522319671e53f6a9ec7a7b0ada70893c69`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 15.0 MB (14957473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef2ef3fb862bd40af56ed9dfb491a632cc83c9dda07d3ed54f62f1656663292`  
		Last Modified: Fri, 23 Jan 2026 01:06:33 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c6b8e8e1f9ae674ef062c57fcda550d4a3c49de5d0e871dba58d8bc1576b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227904442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d3c3aed24ecc7e40cfc3c175bd07b2ec356e596f0255bcd140631ce4333f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:01:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:01:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:01:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:03:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:03:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:03:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:03:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9947ba04387a816becbe01db3421bf1c7dc4c8528a37263103c86be499bd476`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f7658628c43358ae0a387b7155291172c8df22d95994b7809ef3b569e8ff`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bd4aa33571db9327bfd204136c7188ca7f0ef91e3e151de4cf990b06234e09`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 5.8 MB (5793347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b04c03017572da4243cf42c245fa891591da5bbd95eed365edcc4414e057d`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fa0d7a439a243eed55013e1fabbfdc79b33c55685356cd2684838ecf24d172`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057484ee7d655ce804e80ba237690169e818c9795e813adf36ce02ee63c83ed8`  
		Last Modified: Fri, 23 Jan 2026 01:04:05 GMT  
		Size: 48.8 MB (48775856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307bc1b23e39e466e53e917c3fdd0d3d8d9884d2811a9c76f3270c200443e8b`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401192f750876b670a3f1f9b6288280db275be8cac02535d82ebb34828e5f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:07 GMT  
		Size: 126.7 MB (126686219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10258b0bdb1ff25bfa3db6676c3eea41016bf285520c5f1970fac1d68984b145`  
		Last Modified: Fri, 23 Jan 2026 01:04:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707c74cda6ba9b546f57cbb9c61f0ff28c9e7611c87cc4c7ae5b2a236b7d780`  
		Last Modified: Fri, 23 Jan 2026 01:04:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:39564b450e20ae6809cb36690201f3bffc9b573b6aa876dc549acd76b5d4e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49856d28cbca7d55c60db4225aa6786bddf88f220ceddad4044133346b2b7a72`

```dockerfile
```

-	Layers:
	-	`sha256:c3d6fa69dda3c4f16f81b9e7ec1b1c809da1eac3ee3bdfee9f966cb098f90dcd`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 15.0 MB (14955821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e5362a71b82341b3e821eedf97f44ae917116a3a53f883698dcb0ecac329ac`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Wed, 21 Jan 2026 22:50:01 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Wed, 21 Jan 2026 22:50:01 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:7a9d63525e8072408862dd62226440db869e745e37f36968b26e3ef03d6e9641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5aa923a8d649f78968c4db36a83f7173f56d2267742e2f66b7943a08082df623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc31df46db658500d1d56d2037d3b6e564b69de61596b8fcd2ca1be2c9c989b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:05:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:06:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:06:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:06:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9c9ba7072382f7daa02eb7b0d2e620fd996e84a7e2c3f478157c656a4c2615`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be113d11b355d3d5d8ffd0f14b7b2ed4aa30885451c737fe0dc3f8393a69e044`  
		Last Modified: Fri, 23 Jan 2026 01:06:36 GMT  
		Size: 49.9 MB (49923216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bdba0501248e4b8e12eec72b73448109aa526562320546fa27ade027fa72b3`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a2bfb30cdf133ff644108f6f7e6dda508805c52e6c3de2ae396bc9e9f26987`  
		Last Modified: Fri, 23 Jan 2026 01:06:37 GMT  
		Size: 128.1 MB (128104088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ed66656b21312cedae686fa2aaae9f891330d146241e231e45b4a726d9df4a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0ceff8a81bb18f2dfd90b4e468e7d7128cac1376502e996fd4303d924a063a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f51dcb25eecfb1cee34d26e4a601778904eca1835d107a2607a15f629965b36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ac841b89f7909db5fa022b4ec199aada79e7ce4f5c20c060c82b51229488d`

```dockerfile
```

-	Layers:
	-	`sha256:e032523bbbc99c9df18c189f34a21d522319671e53f6a9ec7a7b0ada70893c69`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 15.0 MB (14957473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef2ef3fb862bd40af56ed9dfb491a632cc83c9dda07d3ed54f62f1656663292`  
		Last Modified: Fri, 23 Jan 2026 01:06:33 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c6b8e8e1f9ae674ef062c57fcda550d4a3c49de5d0e871dba58d8bc1576b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227904442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d3c3aed24ecc7e40cfc3c175bd07b2ec356e596f0255bcd140631ce4333f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:01:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:01:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:01:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:03:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:03:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:03:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:03:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9947ba04387a816becbe01db3421bf1c7dc4c8528a37263103c86be499bd476`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f7658628c43358ae0a387b7155291172c8df22d95994b7809ef3b569e8ff`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bd4aa33571db9327bfd204136c7188ca7f0ef91e3e151de4cf990b06234e09`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 5.8 MB (5793347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b04c03017572da4243cf42c245fa891591da5bbd95eed365edcc4414e057d`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fa0d7a439a243eed55013e1fabbfdc79b33c55685356cd2684838ecf24d172`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057484ee7d655ce804e80ba237690169e818c9795e813adf36ce02ee63c83ed8`  
		Last Modified: Fri, 23 Jan 2026 01:04:05 GMT  
		Size: 48.8 MB (48775856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307bc1b23e39e466e53e917c3fdd0d3d8d9884d2811a9c76f3270c200443e8b`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401192f750876b670a3f1f9b6288280db275be8cac02535d82ebb34828e5f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:07 GMT  
		Size: 126.7 MB (126686219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10258b0bdb1ff25bfa3db6676c3eea41016bf285520c5f1970fac1d68984b145`  
		Last Modified: Fri, 23 Jan 2026 01:04:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707c74cda6ba9b546f57cbb9c61f0ff28c9e7611c87cc4c7ae5b2a236b7d780`  
		Last Modified: Fri, 23 Jan 2026 01:04:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:39564b450e20ae6809cb36690201f3bffc9b573b6aa876dc549acd76b5d4e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49856d28cbca7d55c60db4225aa6786bddf88f220ceddad4044133346b2b7a72`

```dockerfile
```

-	Layers:
	-	`sha256:c3d6fa69dda3c4f16f81b9e7ec1b1c809da1eac3ee3bdfee9f966cb098f90dcd`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 15.0 MB (14955821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e5362a71b82341b3e821eedf97f44ae917116a3a53f883698dcb0ecac329ac`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:7a9d63525e8072408862dd62226440db869e745e37f36968b26e3ef03d6e9641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5aa923a8d649f78968c4db36a83f7173f56d2267742e2f66b7943a08082df623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc31df46db658500d1d56d2037d3b6e564b69de61596b8fcd2ca1be2c9c989b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:05:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:06:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:06:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:06:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9c9ba7072382f7daa02eb7b0d2e620fd996e84a7e2c3f478157c656a4c2615`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be113d11b355d3d5d8ffd0f14b7b2ed4aa30885451c737fe0dc3f8393a69e044`  
		Last Modified: Fri, 23 Jan 2026 01:06:36 GMT  
		Size: 49.9 MB (49923216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bdba0501248e4b8e12eec72b73448109aa526562320546fa27ade027fa72b3`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a2bfb30cdf133ff644108f6f7e6dda508805c52e6c3de2ae396bc9e9f26987`  
		Last Modified: Fri, 23 Jan 2026 01:06:37 GMT  
		Size: 128.1 MB (128104088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ed66656b21312cedae686fa2aaae9f891330d146241e231e45b4a726d9df4a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0ceff8a81bb18f2dfd90b4e468e7d7128cac1376502e996fd4303d924a063a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f51dcb25eecfb1cee34d26e4a601778904eca1835d107a2607a15f629965b36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ac841b89f7909db5fa022b4ec199aada79e7ce4f5c20c060c82b51229488d`

```dockerfile
```

-	Layers:
	-	`sha256:e032523bbbc99c9df18c189f34a21d522319671e53f6a9ec7a7b0ada70893c69`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 15.0 MB (14957473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef2ef3fb862bd40af56ed9dfb491a632cc83c9dda07d3ed54f62f1656663292`  
		Last Modified: Fri, 23 Jan 2026 01:06:33 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c6b8e8e1f9ae674ef062c57fcda550d4a3c49de5d0e871dba58d8bc1576b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227904442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d3c3aed24ecc7e40cfc3c175bd07b2ec356e596f0255bcd140631ce4333f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:01:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:01:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:01:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:03:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:03:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:03:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:03:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9947ba04387a816becbe01db3421bf1c7dc4c8528a37263103c86be499bd476`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f7658628c43358ae0a387b7155291172c8df22d95994b7809ef3b569e8ff`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bd4aa33571db9327bfd204136c7188ca7f0ef91e3e151de4cf990b06234e09`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 5.8 MB (5793347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b04c03017572da4243cf42c245fa891591da5bbd95eed365edcc4414e057d`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fa0d7a439a243eed55013e1fabbfdc79b33c55685356cd2684838ecf24d172`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057484ee7d655ce804e80ba237690169e818c9795e813adf36ce02ee63c83ed8`  
		Last Modified: Fri, 23 Jan 2026 01:04:05 GMT  
		Size: 48.8 MB (48775856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307bc1b23e39e466e53e917c3fdd0d3d8d9884d2811a9c76f3270c200443e8b`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401192f750876b670a3f1f9b6288280db275be8cac02535d82ebb34828e5f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:07 GMT  
		Size: 126.7 MB (126686219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10258b0bdb1ff25bfa3db6676c3eea41016bf285520c5f1970fac1d68984b145`  
		Last Modified: Fri, 23 Jan 2026 01:04:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707c74cda6ba9b546f57cbb9c61f0ff28c9e7611c87cc4c7ae5b2a236b7d780`  
		Last Modified: Fri, 23 Jan 2026 01:04:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:39564b450e20ae6809cb36690201f3bffc9b573b6aa876dc549acd76b5d4e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49856d28cbca7d55c60db4225aa6786bddf88f220ceddad4044133346b2b7a72`

```dockerfile
```

-	Layers:
	-	`sha256:c3d6fa69dda3c4f16f81b9e7ec1b1c809da1eac3ee3bdfee9f966cb098f90dcd`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 15.0 MB (14955821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e5362a71b82341b3e821eedf97f44ae917116a3a53f883698dcb0ecac329ac`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:7a9d63525e8072408862dd62226440db869e745e37f36968b26e3ef03d6e9641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:5aa923a8d649f78968c4db36a83f7173f56d2267742e2f66b7943a08082df623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc31df46db658500d1d56d2037d3b6e564b69de61596b8fcd2ca1be2c9c989b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:05:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:06:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:06:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:06:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9c9ba7072382f7daa02eb7b0d2e620fd996e84a7e2c3f478157c656a4c2615`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be113d11b355d3d5d8ffd0f14b7b2ed4aa30885451c737fe0dc3f8393a69e044`  
		Last Modified: Fri, 23 Jan 2026 01:06:36 GMT  
		Size: 49.9 MB (49923216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bdba0501248e4b8e12eec72b73448109aa526562320546fa27ade027fa72b3`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a2bfb30cdf133ff644108f6f7e6dda508805c52e6c3de2ae396bc9e9f26987`  
		Last Modified: Fri, 23 Jan 2026 01:06:37 GMT  
		Size: 128.1 MB (128104088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ed66656b21312cedae686fa2aaae9f891330d146241e231e45b4a726d9df4a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0ceff8a81bb18f2dfd90b4e468e7d7128cac1376502e996fd4303d924a063a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:f51dcb25eecfb1cee34d26e4a601778904eca1835d107a2607a15f629965b36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ac841b89f7909db5fa022b4ec199aada79e7ce4f5c20c060c82b51229488d`

```dockerfile
```

-	Layers:
	-	`sha256:e032523bbbc99c9df18c189f34a21d522319671e53f6a9ec7a7b0ada70893c69`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 15.0 MB (14957473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef2ef3fb862bd40af56ed9dfb491a632cc83c9dda07d3ed54f62f1656663292`  
		Last Modified: Fri, 23 Jan 2026 01:06:33 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c6b8e8e1f9ae674ef062c57fcda550d4a3c49de5d0e871dba58d8bc1576b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227904442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d3c3aed24ecc7e40cfc3c175bd07b2ec356e596f0255bcd140631ce4333f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:01:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:01:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:01:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:03:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:03:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:03:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:03:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9947ba04387a816becbe01db3421bf1c7dc4c8528a37263103c86be499bd476`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f7658628c43358ae0a387b7155291172c8df22d95994b7809ef3b569e8ff`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bd4aa33571db9327bfd204136c7188ca7f0ef91e3e151de4cf990b06234e09`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 5.8 MB (5793347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b04c03017572da4243cf42c245fa891591da5bbd95eed365edcc4414e057d`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fa0d7a439a243eed55013e1fabbfdc79b33c55685356cd2684838ecf24d172`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057484ee7d655ce804e80ba237690169e818c9795e813adf36ce02ee63c83ed8`  
		Last Modified: Fri, 23 Jan 2026 01:04:05 GMT  
		Size: 48.8 MB (48775856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307bc1b23e39e466e53e917c3fdd0d3d8d9884d2811a9c76f3270c200443e8b`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401192f750876b670a3f1f9b6288280db275be8cac02535d82ebb34828e5f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:07 GMT  
		Size: 126.7 MB (126686219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10258b0bdb1ff25bfa3db6676c3eea41016bf285520c5f1970fac1d68984b145`  
		Last Modified: Fri, 23 Jan 2026 01:04:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707c74cda6ba9b546f57cbb9c61f0ff28c9e7611c87cc4c7ae5b2a236b7d780`  
		Last Modified: Fri, 23 Jan 2026 01:04:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:39564b450e20ae6809cb36690201f3bffc9b573b6aa876dc549acd76b5d4e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49856d28cbca7d55c60db4225aa6786bddf88f220ceddad4044133346b2b7a72`

```dockerfile
```

-	Layers:
	-	`sha256:c3d6fa69dda3c4f16f81b9e7ec1b1c809da1eac3ee3bdfee9f966cb098f90dcd`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 15.0 MB (14955821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e5362a71b82341b3e821eedf97f44ae917116a3a53f883698dcb0ecac329ac`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Wed, 21 Jan 2026 22:50:01 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:5284868db9fd4c480d37e8394fb37316ba29b1bdbec31185676faaf42cd82612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:dee7500826371f0383c6673ab1fc4cece140d7f8fb365550597548549b253dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb471428bdc168577f9e02a48169eda26499d392561b1978b431aa483d45e642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 21 Jan 2026 22:49:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 21 Jan 2026 22:49:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 21 Jan 2026 22:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Jan 2026 22:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Jan 2026 22:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 21 Jan 2026 22:49:25 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Wed, 21 Jan 2026 22:49:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 Jan 2026 22:49:36 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 21 Jan 2026 22:49:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jan 2026 22:49:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 21 Jan 2026 22:49:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa36b2e2c985c829bdf403d8168eeae8890c3217a30563a2b5b3aa68e1efdba`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1348177f9534b0b93188d0bd2781bf8088988b503664ef3329e9462ec5e6d`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.4 MB (4423336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cdb304c5842e0232ae8ce1fcf6877cff36e384ba2d8ecc68dd0b670d04f34`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 1.2 MB (1248714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f855ce4e64c494fdd0390394941885efc48adffab2266c04a67f71c80b55fce`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9b517325f53660036f1de6ca0e9494dbc84aafe02d886a34f2bd505a0d80c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 15.3 MB (15295819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94beb5f31bf6179d42df34e5693e2f2e1e7b3efe8ab3be7410347bd25082c2c`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab60d99d7fa5f30783088438eb8f263f39c3c315a7da872044328dd07ca2a26`  
		Last Modified: Wed, 21 Jan 2026 22:49:58 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09fbe4bbb7dde90633da807e1f347b7caf14883cab671790a4369c31ded78f`  
		Last Modified: Wed, 21 Jan 2026 22:50:01 GMT  
		Size: 134.2 MB (134248192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ed9baa1e80f6b50800638f3cdc195044965a20d046ae3565fdfb32a2f8eb6b`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36bcd4939de82e2db98188dc2dd518dbda890712040edb19e8befbbe028557`  
		Last Modified: Wed, 21 Jan 2026 22:49:59 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29984f882141106a3f505fd1ee0d8afaf76a58bf3e0e8f6d953f5bee612777fa`  
		Last Modified: Wed, 21 Jan 2026 22:50:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:a7eddc6833b1dad7a3743fa776da9e6c8604dd9b860673e99b88d15d65e4693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526e7816588d61af24be57343f0050e43cdbbad362b3b6ba103554894ebe19b`

```dockerfile
```

-	Layers:
	-	`sha256:cade0013c36201ab6c42ec4b5f213e754609b2f3fe9fc19478d78770c9747810`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b99cd63676959f0fe9ca9cd457e9c74b4e5e604d39c4d8bca1ba174822cf3c7`  
		Last Modified: Wed, 21 Jan 2026 22:49:57 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:7a9d63525e8072408862dd62226440db869e745e37f36968b26e3ef03d6e9641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5aa923a8d649f78968c4db36a83f7173f56d2267742e2f66b7943a08082df623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc31df46db658500d1d56d2037d3b6e564b69de61596b8fcd2ca1be2c9c989b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:05:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:06:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:06:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:06:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9c9ba7072382f7daa02eb7b0d2e620fd996e84a7e2c3f478157c656a4c2615`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be113d11b355d3d5d8ffd0f14b7b2ed4aa30885451c737fe0dc3f8393a69e044`  
		Last Modified: Fri, 23 Jan 2026 01:06:36 GMT  
		Size: 49.9 MB (49923216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bdba0501248e4b8e12eec72b73448109aa526562320546fa27ade027fa72b3`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a2bfb30cdf133ff644108f6f7e6dda508805c52e6c3de2ae396bc9e9f26987`  
		Last Modified: Fri, 23 Jan 2026 01:06:37 GMT  
		Size: 128.1 MB (128104088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ed66656b21312cedae686fa2aaae9f891330d146241e231e45b4a726d9df4a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0ceff8a81bb18f2dfd90b4e468e7d7128cac1376502e996fd4303d924a063a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f51dcb25eecfb1cee34d26e4a601778904eca1835d107a2607a15f629965b36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ac841b89f7909db5fa022b4ec199aada79e7ce4f5c20c060c82b51229488d`

```dockerfile
```

-	Layers:
	-	`sha256:e032523bbbc99c9df18c189f34a21d522319671e53f6a9ec7a7b0ada70893c69`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 15.0 MB (14957473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef2ef3fb862bd40af56ed9dfb491a632cc83c9dda07d3ed54f62f1656663292`  
		Last Modified: Fri, 23 Jan 2026 01:06:33 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c6b8e8e1f9ae674ef062c57fcda550d4a3c49de5d0e871dba58d8bc1576b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227904442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d3c3aed24ecc7e40cfc3c175bd07b2ec356e596f0255bcd140631ce4333f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:01:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:01:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:01:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:03:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:03:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:03:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:03:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9947ba04387a816becbe01db3421bf1c7dc4c8528a37263103c86be499bd476`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f7658628c43358ae0a387b7155291172c8df22d95994b7809ef3b569e8ff`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bd4aa33571db9327bfd204136c7188ca7f0ef91e3e151de4cf990b06234e09`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 5.8 MB (5793347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b04c03017572da4243cf42c245fa891591da5bbd95eed365edcc4414e057d`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fa0d7a439a243eed55013e1fabbfdc79b33c55685356cd2684838ecf24d172`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057484ee7d655ce804e80ba237690169e818c9795e813adf36ce02ee63c83ed8`  
		Last Modified: Fri, 23 Jan 2026 01:04:05 GMT  
		Size: 48.8 MB (48775856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307bc1b23e39e466e53e917c3fdd0d3d8d9884d2811a9c76f3270c200443e8b`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401192f750876b670a3f1f9b6288280db275be8cac02535d82ebb34828e5f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:07 GMT  
		Size: 126.7 MB (126686219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10258b0bdb1ff25bfa3db6676c3eea41016bf285520c5f1970fac1d68984b145`  
		Last Modified: Fri, 23 Jan 2026 01:04:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707c74cda6ba9b546f57cbb9c61f0ff28c9e7611c87cc4c7ae5b2a236b7d780`  
		Last Modified: Fri, 23 Jan 2026 01:04:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:39564b450e20ae6809cb36690201f3bffc9b573b6aa876dc549acd76b5d4e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49856d28cbca7d55c60db4225aa6786bddf88f220ceddad4044133346b2b7a72`

```dockerfile
```

-	Layers:
	-	`sha256:c3d6fa69dda3c4f16f81b9e7ec1b1c809da1eac3ee3bdfee9f966cb098f90dcd`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 15.0 MB (14955821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e5362a71b82341b3e821eedf97f44ae917116a3a53f883698dcb0ecac329ac`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:7a9d63525e8072408862dd62226440db869e745e37f36968b26e3ef03d6e9641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:5aa923a8d649f78968c4db36a83f7173f56d2267742e2f66b7943a08082df623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232307909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc31df46db658500d1d56d2037d3b6e564b69de61596b8fcd2ca1be2c9c989b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:05:10 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:05:34 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:06:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:06:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:06:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:06:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9c9ba7072382f7daa02eb7b0d2e620fd996e84a7e2c3f478157c656a4c2615`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be113d11b355d3d5d8ffd0f14b7b2ed4aa30885451c737fe0dc3f8393a69e044`  
		Last Modified: Fri, 23 Jan 2026 01:06:36 GMT  
		Size: 49.9 MB (49923216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bdba0501248e4b8e12eec72b73448109aa526562320546fa27ade027fa72b3`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a2bfb30cdf133ff644108f6f7e6dda508805c52e6c3de2ae396bc9e9f26987`  
		Last Modified: Fri, 23 Jan 2026 01:06:37 GMT  
		Size: 128.1 MB (128104088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ed66656b21312cedae686fa2aaae9f891330d146241e231e45b4a726d9df4a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0ceff8a81bb18f2dfd90b4e468e7d7128cac1376502e996fd4303d924a063a`  
		Last Modified: Fri, 23 Jan 2026 01:06:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f51dcb25eecfb1cee34d26e4a601778904eca1835d107a2607a15f629965b36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ac841b89f7909db5fa022b4ec199aada79e7ce4f5c20c060c82b51229488d`

```dockerfile
```

-	Layers:
	-	`sha256:e032523bbbc99c9df18c189f34a21d522319671e53f6a9ec7a7b0ada70893c69`  
		Last Modified: Fri, 23 Jan 2026 01:06:34 GMT  
		Size: 15.0 MB (14957473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef2ef3fb862bd40af56ed9dfb491a632cc83c9dda07d3ed54f62f1656663292`  
		Last Modified: Fri, 23 Jan 2026 01:06:33 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:43c6b8e8e1f9ae674ef062c57fcda550d4a3c49de5d0e871dba58d8bc1576b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227904442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d3c3aed24ecc7e40cfc3c175bd07b2ec356e596f0255bcd140631ce4333f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:01:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:01:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:01:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 23 Jan 2026 01:02:26 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:02:26 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:02:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 23 Jan 2026 01:03:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:03:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:03:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 23 Jan 2026 01:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:03:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9947ba04387a816becbe01db3421bf1c7dc4c8528a37263103c86be499bd476`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28f7658628c43358ae0a387b7155291172c8df22d95994b7809ef3b569e8ff`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 737.5 KB (737521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bd4aa33571db9327bfd204136c7188ca7f0ef91e3e151de4cf990b06234e09`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 5.8 MB (5793347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b04c03017572da4243cf42c245fa891591da5bbd95eed365edcc4414e057d`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fa0d7a439a243eed55013e1fabbfdc79b33c55685356cd2684838ecf24d172`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057484ee7d655ce804e80ba237690169e818c9795e813adf36ce02ee63c83ed8`  
		Last Modified: Fri, 23 Jan 2026 01:04:05 GMT  
		Size: 48.8 MB (48775856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307bc1b23e39e466e53e917c3fdd0d3d8d9884d2811a9c76f3270c200443e8b`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401192f750876b670a3f1f9b6288280db275be8cac02535d82ebb34828e5f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:07 GMT  
		Size: 126.7 MB (126686219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10258b0bdb1ff25bfa3db6676c3eea41016bf285520c5f1970fac1d68984b145`  
		Last Modified: Fri, 23 Jan 2026 01:04:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c707c74cda6ba9b546f57cbb9c61f0ff28c9e7611c87cc4c7ae5b2a236b7d780`  
		Last Modified: Fri, 23 Jan 2026 01:04:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:39564b450e20ae6809cb36690201f3bffc9b573b6aa876dc549acd76b5d4e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49856d28cbca7d55c60db4225aa6786bddf88f220ceddad4044133346b2b7a72`

```dockerfile
```

-	Layers:
	-	`sha256:c3d6fa69dda3c4f16f81b9e7ec1b1c809da1eac3ee3bdfee9f966cb098f90dcd`  
		Last Modified: Fri, 23 Jan 2026 01:04:02 GMT  
		Size: 15.0 MB (14955821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e5362a71b82341b3e821eedf97f44ae917116a3a53f883698dcb0ecac329ac`  
		Last Modified: Fri, 23 Jan 2026 01:04:01 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:63e8ae20eaef51da56723dbeea68dc75e8baa50429f641ba88e8058ce81e17e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:517c70cf9b9a14d9391b4658319b256c4f8ed9f68bd5b644f19915f240445716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233234091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4d755d4d7f8d2ac2693363ddacf5a2246b4357e3260914f019fdcb76ffec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3387bdf9bfcc50f6e9f22d276f8949917a66dc77f6e5a561e7ab21b93ccd1053`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35458f48a115b1ae7b48bf88dea23576e8b9fa8248664a37f58d631335d0b4`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 783.6 KB (783560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bed572afc9f1597e0aff18d190e3c9bafa7cb31d3770470297e86bfd07dc1f6`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 6.2 MB (6173904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e7871685d1219644619bf3123733c6719b4664369161abb47231288ff613be`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc371391c3f95f5514f69669cfba3b262c8edf4767bc5dc6edf87946e68d8d83`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278516eaa73a7b10fb78b22a6d6298d419e3b82e23ff993ecb752cae07cee3d0`  
		Last Modified: Fri, 23 Jan 2026 01:05:02 GMT  
		Size: 47.8 MB (47812418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ee85ca9e5cd28baffa54208769a5935d617e39901bb07212f7ac6e7f55eb30`  
		Last Modified: Fri, 23 Jan 2026 01:05:00 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b24eb35162b54e85382f36d750f37d1fc0f97fb12c1734e115bc2898d79e4d`  
		Last Modified: Fri, 23 Jan 2026 01:05:03 GMT  
		Size: 131.1 MB (131141184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3de5c088871007a9632a30d695159935dad7857e755e96d6ddbd6b4e187e9`  
		Last Modified: Fri, 23 Jan 2026 01:05:01 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f30914a2a465608ed050b05d3feb82143c77ac9c45fb936045d1fa98f61b78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bb69c379d1fc4d60b085fbd0ce36d3decd5d931851ca5b006b67f42042cea`

```dockerfile
```

-	Layers:
	-	`sha256:17ddaa79851b098ef80e51f9edb792248fac6ba08d4e08714b3e2d61e7f077bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 15.2 MB (15234294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb9440a26c8e29f18569864f5cabbeb6d6eeb632460ad2a2931dc475a91ca04`  
		Last Modified: Fri, 23 Jan 2026 01:04:59 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:3212462d5210fb71fa1cf2852ac595395e4c394e1b9ea361d33134e0da3afd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c3411ff7d2d8cb6634704907be187e8bc4b81efd695359e7a511e71059b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:38 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:04 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 23 Jan 2026 01:03:05 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:33 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 23 Jan 2026 01:04:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04773cced5628f77067d61f34f4dfb228b52cb1e4254e5e1533341a2011672a1`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b47139e4337ae96d1dcd7e00aee0c81f2de059f044dd83fa7be2e64a21515`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a56f3f57186c5e12a71e3be69b751079df0b43f1856cadbfa3f17a14dcb8bd`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca0ffa01d79043362e2cd049d24bd013d2fd74f341681ff7fc9e03e265ee3b7`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095054a92a30ea20e57a323f3e73ebf25c905e593768d961d8f2fb8713cdb61`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4775faeffd0ab7361b4f21f852ad5527af992fab942c20a95ade600579909ebe`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 46.7 MB (46699432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08698bbb53add1b4beff38debd565f562b7a1e8b0ac24e70354e7848d37e423`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4623e1c2a43d854c41086f4da6b7eef8ea9d19029a87d361b07c792ad309498f`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 129.6 MB (129550743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d000b5afec14090e7bc0fa5151982e7fbafd6ddfe9ee29dcce9b1f74e85ed1`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:397075b87a78f4d001164584db6a9fcad1c039bcc852415b600de4b560d35681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ffb50a15d89438d37d6be7c36144fbd0c0628ff131ee585a629d23c2767c1e`

```dockerfile
```

-	Layers:
	-	`sha256:77f59b0dee93e8a07187032df8a8ca56eae940b467367ed6f8fe00faf7a7451d`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 15.2 MB (15232714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc1d13ac487aca899d20bfc92219122fb4ddae0228ad6e5745352e8d1697db6`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
