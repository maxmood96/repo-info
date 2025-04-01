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
-	[`mysql:8.0.41`](#mysql8041)
-	[`mysql:8.0.41-bookworm`](#mysql8041-bookworm)
-	[`mysql:8.0.41-debian`](#mysql8041-debian)
-	[`mysql:8.0.41-oracle`](#mysql8041-oracle)
-	[`mysql:8.0.41-oraclelinux9`](#mysql8041-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.4`](#mysql844)
-	[`mysql:8.4.4-oracle`](#mysql844-oracle)
-	[`mysql:8.4.4-oraclelinux9`](#mysql844-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.2`](#mysql92)
-	[`mysql:9.2-oracle`](#mysql92-oracle)
-	[`mysql:9.2-oraclelinux9`](#mysql92-oraclelinux9)
-	[`mysql:9.2.0`](#mysql920)
-	[`mysql:9.2.0-oracle`](#mysql920-oracle)
-	[`mysql:9.2.0-oraclelinux9`](#mysql920-oraclelinux9)
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
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:bf577825b52ab281d6281fb281eabbfdc73507eda8f2c2745790251533ef0306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:d226408713974bd903e3bc40d0dc5d345e2e2e12131222de6ec4fba0e82fbec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231892794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c83f38450c378c8df08cc10dd46400d17a404c68a63cf92ccfb49fb75b9cdfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e01aa53f130b16e98816d9fe2e1dc21636134c214d3b65e5ad566d60190aa6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa3211d7a79e4f130ac9b19c89a8e043d9c0e71ea8a5bde8876a8fb16c5c57`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b8441f7e648598e48060ba5c31234e938275cfbf111be1392770e8fc2bf81`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 6.9 MB (6896548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1339a14fa1aef8fb560649d4138db3ec7b3335fe8acfd781aa8eb15af0da7b6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be386ff914e324930070097d9769b5fdfe58e26578655ff6a8f7349c6a85abeb`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93272c957f26f911d8a81573597702f0483e85a17b881c519b55d08dd1c508cc`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 49.6 MB (49623014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c106a4902288ff406ad412356aff079242c25540993b518577479b1247eea14e`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f4325df2da36f080083cd04e3944694119218502ec02a13e23dd763186ed9`  
		Last Modified: Tue, 01 Apr 2025 01:09:08 GMT  
		Size: 125.3 MB (125289436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d34979e71209018c014bc4ad0c225c3ceeacdb4dc4b6ae2483ea41bf1697d90`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67a2f637e5925ad6234ae9659c12e6a0c85cc7d7c90a2a37b42f24ce578b08`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:a8fe37e7dbfbe9fab2beddec5cd3667d13c5917e61dec6f1537f17c73bbbb06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5016c97d6b63ca4c43b50f5e3e18de3d5e5f7173029c6bf3de434880b3a30518`

```dockerfile
```

-	Layers:
	-	`sha256:865fcd219464e01b058eaf95e278b582f6b16bd4833d02c8679702a8d5f8da04`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 13.8 MB (13798499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a482f56def3566f08062888ebc42c26679685e440b2497f90b52f16877485dbc`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e682bf746a8539c46e1377f18a8b10c5270c077e88e5949c508356bbd33fd93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227529930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cbefe8f93260ad63735dad3774e719ce68478b1f52d2f582fd3ddaa452525e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af997c5168ac919e485cf505263301cc2f22335ac58da23fd8611adea2709f9`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4da0fef3d8b01b12e3b497f14c1ae17d29384d743a97036eaa81959929ff7`  
		Last Modified: Tue, 01 Apr 2025 01:12:02 GMT  
		Size: 48.5 MB (48502864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6940dbb4eace389b86369512adf6a18f6311ad20cef2aaaca05a82a88fa8190b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15896173647efcd0af5c7a09e6ea607d3ffcefea982e183ff42c72e8a1b47dcc`  
		Last Modified: Tue, 01 Apr 2025 01:12:05 GMT  
		Size: 123.9 MB (123938905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d63cb0124df7cd6823c58a825ae7e65cdd1047e44cf2d14edae2f255c11f3`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bda411c15dea823c62ba1e673a769ec06cd1bfb77a4407f6581b9af32c191c`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:38d33f636c125c09c26ced7c1239d944efd8bf10dd45d72d17f3325f0da4455e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd144a577b0eb5095d3d531952845826d36bf7d17287af129c225498dbfa3e`

```dockerfile
```

-	Layers:
	-	`sha256:72807f421c116aad6b03c0ec6d2fa993a965f55dced52629d0264cbb0c53cbd4`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 13.8 MB (13796847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f062916e36483fca39b7eae52663242911e22e6526cc0abbcfa7b15f1c3471b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:4e503fc27366cedcf545f103d2d3a447c1daf69083e976863206812f5b0ab5dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:54f4a132cc9de5e9ec03f5e21bf5e332a43a586fb29f956443035e44ca446c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183291055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ca72b6e3818215f114d8783043a792359de4d79a6b23722428c2b9783da45f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b158c169f05037fd56a7528468d5a8f5081f5c3221c45fa1c6c5fbfbfb88ef1`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a845a93afa96756147b6a38f09cb198ceafa11ea12d31d2596f3a97b1ade77`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 4.4 MB (4422827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cea16c8d9b3397320dfab40d3b93baa575d03948c4c8c9433c284014f6c617`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 1.4 MB (1445989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd9f0d9155e0bc3fac666c73343001fa6bb2709f06f479018a2b5b0ac461d4`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d47fc5041b3ffc651f90654a8cadb2667846d313fbb8132a6035cf2274e71d0`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 15.3 MB (15296639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49f8d35697a69010c85ef891b036ee03932e60aacdc1cd95414a8350d7bc8da`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c914949f8f1157aaf4bf365c4ea1ff4855da56235b15264a3642ded9ff003f`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9009038023a85736876efc7cd0e05e2b1545154c9cae9260b68a22ca8942eb1`  
		Last Modified: Mon, 17 Mar 2025 23:14:54 GMT  
		Size: 133.9 MB (133910467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4cd08717fd0ddcb09c167567d334f6a2ce14614ca541f147b0be1a9774ed`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947a0da90cfab682c72bea2c41cf9f692ecbe09fd611bb812b671701a81a6e6`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5618945424910e4780fe27597d8e8f0b9ff78de67ec0feaf2199596373af0cc2`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:a16de2fcf677f589150d54157471faf776103e24bb9e196c7d2a5fb9129092e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f1a2e12916175fa9c4e75dd82c0334709041d33fbea9c0913574d1951f9572`

```dockerfile
```

-	Layers:
	-	`sha256:e5548e8108d6e6b3cfb5b63e559e05202cf1f86dbff1775f4235d1ef5c1bbfff`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 4.0 MB (3993834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30093275186b95e820bd47703c8fc2dd4d087bfc452d8426e0f96c2c352b78f8`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:4e503fc27366cedcf545f103d2d3a447c1daf69083e976863206812f5b0ab5dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:54f4a132cc9de5e9ec03f5e21bf5e332a43a586fb29f956443035e44ca446c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183291055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ca72b6e3818215f114d8783043a792359de4d79a6b23722428c2b9783da45f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b158c169f05037fd56a7528468d5a8f5081f5c3221c45fa1c6c5fbfbfb88ef1`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a845a93afa96756147b6a38f09cb198ceafa11ea12d31d2596f3a97b1ade77`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 4.4 MB (4422827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cea16c8d9b3397320dfab40d3b93baa575d03948c4c8c9433c284014f6c617`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 1.4 MB (1445989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd9f0d9155e0bc3fac666c73343001fa6bb2709f06f479018a2b5b0ac461d4`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d47fc5041b3ffc651f90654a8cadb2667846d313fbb8132a6035cf2274e71d0`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 15.3 MB (15296639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49f8d35697a69010c85ef891b036ee03932e60aacdc1cd95414a8350d7bc8da`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c914949f8f1157aaf4bf365c4ea1ff4855da56235b15264a3642ded9ff003f`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9009038023a85736876efc7cd0e05e2b1545154c9cae9260b68a22ca8942eb1`  
		Last Modified: Mon, 17 Mar 2025 23:14:54 GMT  
		Size: 133.9 MB (133910467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4cd08717fd0ddcb09c167567d334f6a2ce14614ca541f147b0be1a9774ed`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947a0da90cfab682c72bea2c41cf9f692ecbe09fd611bb812b671701a81a6e6`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5618945424910e4780fe27597d8e8f0b9ff78de67ec0feaf2199596373af0cc2`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:a16de2fcf677f589150d54157471faf776103e24bb9e196c7d2a5fb9129092e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f1a2e12916175fa9c4e75dd82c0334709041d33fbea9c0913574d1951f9572`

```dockerfile
```

-	Layers:
	-	`sha256:e5548e8108d6e6b3cfb5b63e559e05202cf1f86dbff1775f4235d1ef5c1bbfff`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 4.0 MB (3993834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30093275186b95e820bd47703c8fc2dd4d087bfc452d8426e0f96c2c352b78f8`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:bf577825b52ab281d6281fb281eabbfdc73507eda8f2c2745790251533ef0306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d226408713974bd903e3bc40d0dc5d345e2e2e12131222de6ec4fba0e82fbec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231892794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c83f38450c378c8df08cc10dd46400d17a404c68a63cf92ccfb49fb75b9cdfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e01aa53f130b16e98816d9fe2e1dc21636134c214d3b65e5ad566d60190aa6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa3211d7a79e4f130ac9b19c89a8e043d9c0e71ea8a5bde8876a8fb16c5c57`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b8441f7e648598e48060ba5c31234e938275cfbf111be1392770e8fc2bf81`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 6.9 MB (6896548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1339a14fa1aef8fb560649d4138db3ec7b3335fe8acfd781aa8eb15af0da7b6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be386ff914e324930070097d9769b5fdfe58e26578655ff6a8f7349c6a85abeb`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93272c957f26f911d8a81573597702f0483e85a17b881c519b55d08dd1c508cc`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 49.6 MB (49623014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c106a4902288ff406ad412356aff079242c25540993b518577479b1247eea14e`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f4325df2da36f080083cd04e3944694119218502ec02a13e23dd763186ed9`  
		Last Modified: Tue, 01 Apr 2025 01:09:08 GMT  
		Size: 125.3 MB (125289436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d34979e71209018c014bc4ad0c225c3ceeacdb4dc4b6ae2483ea41bf1697d90`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67a2f637e5925ad6234ae9659c12e6a0c85cc7d7c90a2a37b42f24ce578b08`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a8fe37e7dbfbe9fab2beddec5cd3667d13c5917e61dec6f1537f17c73bbbb06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5016c97d6b63ca4c43b50f5e3e18de3d5e5f7173029c6bf3de434880b3a30518`

```dockerfile
```

-	Layers:
	-	`sha256:865fcd219464e01b058eaf95e278b582f6b16bd4833d02c8679702a8d5f8da04`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 13.8 MB (13798499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a482f56def3566f08062888ebc42c26679685e440b2497f90b52f16877485dbc`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e682bf746a8539c46e1377f18a8b10c5270c077e88e5949c508356bbd33fd93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227529930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cbefe8f93260ad63735dad3774e719ce68478b1f52d2f582fd3ddaa452525e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af997c5168ac919e485cf505263301cc2f22335ac58da23fd8611adea2709f9`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4da0fef3d8b01b12e3b497f14c1ae17d29384d743a97036eaa81959929ff7`  
		Last Modified: Tue, 01 Apr 2025 01:12:02 GMT  
		Size: 48.5 MB (48502864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6940dbb4eace389b86369512adf6a18f6311ad20cef2aaaca05a82a88fa8190b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15896173647efcd0af5c7a09e6ea607d3ffcefea982e183ff42c72e8a1b47dcc`  
		Last Modified: Tue, 01 Apr 2025 01:12:05 GMT  
		Size: 123.9 MB (123938905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d63cb0124df7cd6823c58a825ae7e65cdd1047e44cf2d14edae2f255c11f3`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bda411c15dea823c62ba1e673a769ec06cd1bfb77a4407f6581b9af32c191c`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:38d33f636c125c09c26ced7c1239d944efd8bf10dd45d72d17f3325f0da4455e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd144a577b0eb5095d3d531952845826d36bf7d17287af129c225498dbfa3e`

```dockerfile
```

-	Layers:
	-	`sha256:72807f421c116aad6b03c0ec6d2fa993a965f55dced52629d0264cbb0c53cbd4`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 13.8 MB (13796847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f062916e36483fca39b7eae52663242911e22e6526cc0abbcfa7b15f1c3471b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:bf577825b52ab281d6281fb281eabbfdc73507eda8f2c2745790251533ef0306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d226408713974bd903e3bc40d0dc5d345e2e2e12131222de6ec4fba0e82fbec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231892794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c83f38450c378c8df08cc10dd46400d17a404c68a63cf92ccfb49fb75b9cdfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e01aa53f130b16e98816d9fe2e1dc21636134c214d3b65e5ad566d60190aa6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa3211d7a79e4f130ac9b19c89a8e043d9c0e71ea8a5bde8876a8fb16c5c57`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b8441f7e648598e48060ba5c31234e938275cfbf111be1392770e8fc2bf81`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 6.9 MB (6896548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1339a14fa1aef8fb560649d4138db3ec7b3335fe8acfd781aa8eb15af0da7b6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be386ff914e324930070097d9769b5fdfe58e26578655ff6a8f7349c6a85abeb`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93272c957f26f911d8a81573597702f0483e85a17b881c519b55d08dd1c508cc`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 49.6 MB (49623014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c106a4902288ff406ad412356aff079242c25540993b518577479b1247eea14e`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f4325df2da36f080083cd04e3944694119218502ec02a13e23dd763186ed9`  
		Last Modified: Tue, 01 Apr 2025 01:09:08 GMT  
		Size: 125.3 MB (125289436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d34979e71209018c014bc4ad0c225c3ceeacdb4dc4b6ae2483ea41bf1697d90`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67a2f637e5925ad6234ae9659c12e6a0c85cc7d7c90a2a37b42f24ce578b08`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a8fe37e7dbfbe9fab2beddec5cd3667d13c5917e61dec6f1537f17c73bbbb06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5016c97d6b63ca4c43b50f5e3e18de3d5e5f7173029c6bf3de434880b3a30518`

```dockerfile
```

-	Layers:
	-	`sha256:865fcd219464e01b058eaf95e278b582f6b16bd4833d02c8679702a8d5f8da04`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 13.8 MB (13798499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a482f56def3566f08062888ebc42c26679685e440b2497f90b52f16877485dbc`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e682bf746a8539c46e1377f18a8b10c5270c077e88e5949c508356bbd33fd93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227529930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cbefe8f93260ad63735dad3774e719ce68478b1f52d2f582fd3ddaa452525e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af997c5168ac919e485cf505263301cc2f22335ac58da23fd8611adea2709f9`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4da0fef3d8b01b12e3b497f14c1ae17d29384d743a97036eaa81959929ff7`  
		Last Modified: Tue, 01 Apr 2025 01:12:02 GMT  
		Size: 48.5 MB (48502864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6940dbb4eace389b86369512adf6a18f6311ad20cef2aaaca05a82a88fa8190b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15896173647efcd0af5c7a09e6ea607d3ffcefea982e183ff42c72e8a1b47dcc`  
		Last Modified: Tue, 01 Apr 2025 01:12:05 GMT  
		Size: 123.9 MB (123938905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d63cb0124df7cd6823c58a825ae7e65cdd1047e44cf2d14edae2f255c11f3`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bda411c15dea823c62ba1e673a769ec06cd1bfb77a4407f6581b9af32c191c`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:38d33f636c125c09c26ced7c1239d944efd8bf10dd45d72d17f3325f0da4455e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd144a577b0eb5095d3d531952845826d36bf7d17287af129c225498dbfa3e`

```dockerfile
```

-	Layers:
	-	`sha256:72807f421c116aad6b03c0ec6d2fa993a965f55dced52629d0264cbb0c53cbd4`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 13.8 MB (13796847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f062916e36483fca39b7eae52663242911e22e6526cc0abbcfa7b15f1c3471b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41`

```console
$ docker pull mysql@sha256:bf577825b52ab281d6281fb281eabbfdc73507eda8f2c2745790251533ef0306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41` - linux; amd64

```console
$ docker pull mysql@sha256:d226408713974bd903e3bc40d0dc5d345e2e2e12131222de6ec4fba0e82fbec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231892794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c83f38450c378c8df08cc10dd46400d17a404c68a63cf92ccfb49fb75b9cdfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e01aa53f130b16e98816d9fe2e1dc21636134c214d3b65e5ad566d60190aa6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa3211d7a79e4f130ac9b19c89a8e043d9c0e71ea8a5bde8876a8fb16c5c57`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b8441f7e648598e48060ba5c31234e938275cfbf111be1392770e8fc2bf81`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 6.9 MB (6896548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1339a14fa1aef8fb560649d4138db3ec7b3335fe8acfd781aa8eb15af0da7b6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be386ff914e324930070097d9769b5fdfe58e26578655ff6a8f7349c6a85abeb`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93272c957f26f911d8a81573597702f0483e85a17b881c519b55d08dd1c508cc`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 49.6 MB (49623014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c106a4902288ff406ad412356aff079242c25540993b518577479b1247eea14e`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f4325df2da36f080083cd04e3944694119218502ec02a13e23dd763186ed9`  
		Last Modified: Tue, 01 Apr 2025 01:09:08 GMT  
		Size: 125.3 MB (125289436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d34979e71209018c014bc4ad0c225c3ceeacdb4dc4b6ae2483ea41bf1697d90`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67a2f637e5925ad6234ae9659c12e6a0c85cc7d7c90a2a37b42f24ce578b08`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41` - unknown; unknown

```console
$ docker pull mysql@sha256:a8fe37e7dbfbe9fab2beddec5cd3667d13c5917e61dec6f1537f17c73bbbb06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5016c97d6b63ca4c43b50f5e3e18de3d5e5f7173029c6bf3de434880b3a30518`

```dockerfile
```

-	Layers:
	-	`sha256:865fcd219464e01b058eaf95e278b582f6b16bd4833d02c8679702a8d5f8da04`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 13.8 MB (13798499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a482f56def3566f08062888ebc42c26679685e440b2497f90b52f16877485dbc`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e682bf746a8539c46e1377f18a8b10c5270c077e88e5949c508356bbd33fd93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227529930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cbefe8f93260ad63735dad3774e719ce68478b1f52d2f582fd3ddaa452525e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af997c5168ac919e485cf505263301cc2f22335ac58da23fd8611adea2709f9`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4da0fef3d8b01b12e3b497f14c1ae17d29384d743a97036eaa81959929ff7`  
		Last Modified: Tue, 01 Apr 2025 01:12:02 GMT  
		Size: 48.5 MB (48502864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6940dbb4eace389b86369512adf6a18f6311ad20cef2aaaca05a82a88fa8190b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15896173647efcd0af5c7a09e6ea607d3ffcefea982e183ff42c72e8a1b47dcc`  
		Last Modified: Tue, 01 Apr 2025 01:12:05 GMT  
		Size: 123.9 MB (123938905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d63cb0124df7cd6823c58a825ae7e65cdd1047e44cf2d14edae2f255c11f3`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bda411c15dea823c62ba1e673a769ec06cd1bfb77a4407f6581b9af32c191c`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41` - unknown; unknown

```console
$ docker pull mysql@sha256:38d33f636c125c09c26ced7c1239d944efd8bf10dd45d72d17f3325f0da4455e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd144a577b0eb5095d3d531952845826d36bf7d17287af129c225498dbfa3e`

```dockerfile
```

-	Layers:
	-	`sha256:72807f421c116aad6b03c0ec6d2fa993a965f55dced52629d0264cbb0c53cbd4`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 13.8 MB (13796847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f062916e36483fca39b7eae52663242911e22e6526cc0abbcfa7b15f1c3471b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-bookworm`

```console
$ docker pull mysql@sha256:4e503fc27366cedcf545f103d2d3a447c1daf69083e976863206812f5b0ab5dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.41-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:54f4a132cc9de5e9ec03f5e21bf5e332a43a586fb29f956443035e44ca446c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183291055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ca72b6e3818215f114d8783043a792359de4d79a6b23722428c2b9783da45f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b158c169f05037fd56a7528468d5a8f5081f5c3221c45fa1c6c5fbfbfb88ef1`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a845a93afa96756147b6a38f09cb198ceafa11ea12d31d2596f3a97b1ade77`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 4.4 MB (4422827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cea16c8d9b3397320dfab40d3b93baa575d03948c4c8c9433c284014f6c617`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 1.4 MB (1445989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd9f0d9155e0bc3fac666c73343001fa6bb2709f06f479018a2b5b0ac461d4`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d47fc5041b3ffc651f90654a8cadb2667846d313fbb8132a6035cf2274e71d0`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 15.3 MB (15296639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49f8d35697a69010c85ef891b036ee03932e60aacdc1cd95414a8350d7bc8da`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c914949f8f1157aaf4bf365c4ea1ff4855da56235b15264a3642ded9ff003f`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9009038023a85736876efc7cd0e05e2b1545154c9cae9260b68a22ca8942eb1`  
		Last Modified: Mon, 17 Mar 2025 23:14:54 GMT  
		Size: 133.9 MB (133910467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4cd08717fd0ddcb09c167567d334f6a2ce14614ca541f147b0be1a9774ed`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947a0da90cfab682c72bea2c41cf9f692ecbe09fd611bb812b671701a81a6e6`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5618945424910e4780fe27597d8e8f0b9ff78de67ec0feaf2199596373af0cc2`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:a16de2fcf677f589150d54157471faf776103e24bb9e196c7d2a5fb9129092e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f1a2e12916175fa9c4e75dd82c0334709041d33fbea9c0913574d1951f9572`

```dockerfile
```

-	Layers:
	-	`sha256:e5548e8108d6e6b3cfb5b63e559e05202cf1f86dbff1775f4235d1ef5c1bbfff`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 4.0 MB (3993834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30093275186b95e820bd47703c8fc2dd4d087bfc452d8426e0f96c2c352b78f8`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-debian`

```console
$ docker pull mysql@sha256:4e503fc27366cedcf545f103d2d3a447c1daf69083e976863206812f5b0ab5dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:54f4a132cc9de5e9ec03f5e21bf5e332a43a586fb29f956443035e44ca446c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183291055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ca72b6e3818215f114d8783043a792359de4d79a6b23722428c2b9783da45f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b158c169f05037fd56a7528468d5a8f5081f5c3221c45fa1c6c5fbfbfb88ef1`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a845a93afa96756147b6a38f09cb198ceafa11ea12d31d2596f3a97b1ade77`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 4.4 MB (4422827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cea16c8d9b3397320dfab40d3b93baa575d03948c4c8c9433c284014f6c617`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 1.4 MB (1445989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd9f0d9155e0bc3fac666c73343001fa6bb2709f06f479018a2b5b0ac461d4`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d47fc5041b3ffc651f90654a8cadb2667846d313fbb8132a6035cf2274e71d0`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 15.3 MB (15296639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49f8d35697a69010c85ef891b036ee03932e60aacdc1cd95414a8350d7bc8da`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c914949f8f1157aaf4bf365c4ea1ff4855da56235b15264a3642ded9ff003f`  
		Last Modified: Mon, 17 Mar 2025 23:14:52 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9009038023a85736876efc7cd0e05e2b1545154c9cae9260b68a22ca8942eb1`  
		Last Modified: Mon, 17 Mar 2025 23:14:54 GMT  
		Size: 133.9 MB (133910467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c4cd08717fd0ddcb09c167567d334f6a2ce14614ca541f147b0be1a9774ed`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c947a0da90cfab682c72bea2c41cf9f692ecbe09fd611bb812b671701a81a6e6`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5618945424910e4780fe27597d8e8f0b9ff78de67ec0feaf2199596373af0cc2`  
		Last Modified: Mon, 17 Mar 2025 23:14:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:a16de2fcf677f589150d54157471faf776103e24bb9e196c7d2a5fb9129092e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f1a2e12916175fa9c4e75dd82c0334709041d33fbea9c0913574d1951f9572`

```dockerfile
```

-	Layers:
	-	`sha256:e5548e8108d6e6b3cfb5b63e559e05202cf1f86dbff1775f4235d1ef5c1bbfff`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 4.0 MB (3993834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30093275186b95e820bd47703c8fc2dd4d087bfc452d8426e0f96c2c352b78f8`  
		Last Modified: Mon, 17 Mar 2025 23:14:51 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-oracle`

```console
$ docker pull mysql@sha256:bf577825b52ab281d6281fb281eabbfdc73507eda8f2c2745790251533ef0306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d226408713974bd903e3bc40d0dc5d345e2e2e12131222de6ec4fba0e82fbec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231892794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c83f38450c378c8df08cc10dd46400d17a404c68a63cf92ccfb49fb75b9cdfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e01aa53f130b16e98816d9fe2e1dc21636134c214d3b65e5ad566d60190aa6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa3211d7a79e4f130ac9b19c89a8e043d9c0e71ea8a5bde8876a8fb16c5c57`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b8441f7e648598e48060ba5c31234e938275cfbf111be1392770e8fc2bf81`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 6.9 MB (6896548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1339a14fa1aef8fb560649d4138db3ec7b3335fe8acfd781aa8eb15af0da7b6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be386ff914e324930070097d9769b5fdfe58e26578655ff6a8f7349c6a85abeb`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93272c957f26f911d8a81573597702f0483e85a17b881c519b55d08dd1c508cc`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 49.6 MB (49623014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c106a4902288ff406ad412356aff079242c25540993b518577479b1247eea14e`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f4325df2da36f080083cd04e3944694119218502ec02a13e23dd763186ed9`  
		Last Modified: Tue, 01 Apr 2025 01:09:08 GMT  
		Size: 125.3 MB (125289436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d34979e71209018c014bc4ad0c225c3ceeacdb4dc4b6ae2483ea41bf1697d90`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67a2f637e5925ad6234ae9659c12e6a0c85cc7d7c90a2a37b42f24ce578b08`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a8fe37e7dbfbe9fab2beddec5cd3667d13c5917e61dec6f1537f17c73bbbb06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5016c97d6b63ca4c43b50f5e3e18de3d5e5f7173029c6bf3de434880b3a30518`

```dockerfile
```

-	Layers:
	-	`sha256:865fcd219464e01b058eaf95e278b582f6b16bd4833d02c8679702a8d5f8da04`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 13.8 MB (13798499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a482f56def3566f08062888ebc42c26679685e440b2497f90b52f16877485dbc`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e682bf746a8539c46e1377f18a8b10c5270c077e88e5949c508356bbd33fd93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227529930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cbefe8f93260ad63735dad3774e719ce68478b1f52d2f582fd3ddaa452525e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af997c5168ac919e485cf505263301cc2f22335ac58da23fd8611adea2709f9`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4da0fef3d8b01b12e3b497f14c1ae17d29384d743a97036eaa81959929ff7`  
		Last Modified: Tue, 01 Apr 2025 01:12:02 GMT  
		Size: 48.5 MB (48502864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6940dbb4eace389b86369512adf6a18f6311ad20cef2aaaca05a82a88fa8190b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15896173647efcd0af5c7a09e6ea607d3ffcefea982e183ff42c72e8a1b47dcc`  
		Last Modified: Tue, 01 Apr 2025 01:12:05 GMT  
		Size: 123.9 MB (123938905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d63cb0124df7cd6823c58a825ae7e65cdd1047e44cf2d14edae2f255c11f3`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bda411c15dea823c62ba1e673a769ec06cd1bfb77a4407f6581b9af32c191c`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:38d33f636c125c09c26ced7c1239d944efd8bf10dd45d72d17f3325f0da4455e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd144a577b0eb5095d3d531952845826d36bf7d17287af129c225498dbfa3e`

```dockerfile
```

-	Layers:
	-	`sha256:72807f421c116aad6b03c0ec6d2fa993a965f55dced52629d0264cbb0c53cbd4`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 13.8 MB (13796847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f062916e36483fca39b7eae52663242911e22e6526cc0abbcfa7b15f1c3471b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-oraclelinux9`

```console
$ docker pull mysql@sha256:bf577825b52ab281d6281fb281eabbfdc73507eda8f2c2745790251533ef0306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d226408713974bd903e3bc40d0dc5d345e2e2e12131222de6ec4fba0e82fbec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231892794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c83f38450c378c8df08cc10dd46400d17a404c68a63cf92ccfb49fb75b9cdfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e01aa53f130b16e98816d9fe2e1dc21636134c214d3b65e5ad566d60190aa6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa3211d7a79e4f130ac9b19c89a8e043d9c0e71ea8a5bde8876a8fb16c5c57`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b8441f7e648598e48060ba5c31234e938275cfbf111be1392770e8fc2bf81`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 6.9 MB (6896548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1339a14fa1aef8fb560649d4138db3ec7b3335fe8acfd781aa8eb15af0da7b6`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be386ff914e324930070097d9769b5fdfe58e26578655ff6a8f7349c6a85abeb`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93272c957f26f911d8a81573597702f0483e85a17b881c519b55d08dd1c508cc`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 49.6 MB (49623014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c106a4902288ff406ad412356aff079242c25540993b518577479b1247eea14e`  
		Last Modified: Tue, 01 Apr 2025 01:09:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f4325df2da36f080083cd04e3944694119218502ec02a13e23dd763186ed9`  
		Last Modified: Tue, 01 Apr 2025 01:09:08 GMT  
		Size: 125.3 MB (125289436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d34979e71209018c014bc4ad0c225c3ceeacdb4dc4b6ae2483ea41bf1697d90`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67a2f637e5925ad6234ae9659c12e6a0c85cc7d7c90a2a37b42f24ce578b08`  
		Last Modified: Tue, 01 Apr 2025 01:09:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a8fe37e7dbfbe9fab2beddec5cd3667d13c5917e61dec6f1537f17c73bbbb06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5016c97d6b63ca4c43b50f5e3e18de3d5e5f7173029c6bf3de434880b3a30518`

```dockerfile
```

-	Layers:
	-	`sha256:865fcd219464e01b058eaf95e278b582f6b16bd4833d02c8679702a8d5f8da04`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 13.8 MB (13798499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a482f56def3566f08062888ebc42c26679685e440b2497f90b52f16877485dbc`  
		Last Modified: Tue, 01 Apr 2025 01:09:05 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e682bf746a8539c46e1377f18a8b10c5270c077e88e5949c508356bbd33fd93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227529930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cbefe8f93260ad63735dad3774e719ce68478b1f52d2f582fd3ddaa452525e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:15:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af997c5168ac919e485cf505263301cc2f22335ac58da23fd8611adea2709f9`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4da0fef3d8b01b12e3b497f14c1ae17d29384d743a97036eaa81959929ff7`  
		Last Modified: Tue, 01 Apr 2025 01:12:02 GMT  
		Size: 48.5 MB (48502864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6940dbb4eace389b86369512adf6a18f6311ad20cef2aaaca05a82a88fa8190b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15896173647efcd0af5c7a09e6ea607d3ffcefea982e183ff42c72e8a1b47dcc`  
		Last Modified: Tue, 01 Apr 2025 01:12:05 GMT  
		Size: 123.9 MB (123938905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d63cb0124df7cd6823c58a825ae7e65cdd1047e44cf2d14edae2f255c11f3`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bda411c15dea823c62ba1e673a769ec06cd1bfb77a4407f6581b9af32c191c`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:38d33f636c125c09c26ced7c1239d944efd8bf10dd45d72d17f3325f0da4455e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd144a577b0eb5095d3d531952845826d36bf7d17287af129c225498dbfa3e`

```dockerfile
```

-	Layers:
	-	`sha256:72807f421c116aad6b03c0ec6d2fa993a965f55dced52629d0264cbb0c53cbd4`  
		Last Modified: Tue, 01 Apr 2025 01:12:01 GMT  
		Size: 13.8 MB (13796847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f062916e36483fca39b7eae52663242911e22e6526cc0abbcfa7b15f1c3471b`  
		Last Modified: Tue, 01 Apr 2025 01:12:00 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4-oracle`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4-oraclelinux9`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2-oracle`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2-oraclelinux9`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0-oracle`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0-oraclelinux9`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:23818b7d7de427096ab1427b2e3d9d5e14a5b933f9a4431a482d6414bc879091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d895a591bdc9fbd228dc75f4859791160f321b839bad18bba44811834143b0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232885973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a163431d31522cab6c335566e006ae179bd53b0c7bb3bcac4a2484d5daf72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0eb82d78dcf44efd1e3f6adc0971f7ebccf4862c2c00ca189f9fabf81a0839`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667541f13f540da4118d39dacba6fe29774c6162e338d0bb7c357f104d02c2`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fefeb7f3b5238755805e5a7f095c28531bd489090de3ba4046b429fdb067c7`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 6.9 MB (6896403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7405f0a17cb41b76837c697cca8f9ae04f324794027f12de583054cd148948`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cefcf2c6413905921fd84edbaa0a60163358ea96d99ef39ffe7caa2280160c`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38945ff9f35a170ce7e01bc20b9f7220c8bed0250eeb25471ca98ad2ed32625d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 47.6 MB (47584669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd4b133d74634ade078bdc5ffdf89fd03dd4972f181658e6be6938f7647ee9`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4511c9955c0d4c79336f3ab6864cb6cd967351b65df8c6b96fea93b2d07ade6`  
		Last Modified: Tue, 01 Apr 2025 01:09:03 GMT  
		Size: 128.3 MB (128321215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014654182aa239ad2cfa47f377b352cbaaa20a708a729c74256fd44cbce3ce5d`  
		Last Modified: Tue, 01 Apr 2025 01:09:01 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:cd6c1ee1fad4cad7dce6be8b9dddb39018ad2fb9611ef6c160dde457519b1ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14109570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea93d1cb40cfda998be62f86333e519a83f59835903f2eed0763782354d7d018`

```dockerfile
```

-	Layers:
	-	`sha256:0eaae68644e93f2c44114ba5e857524d176f2ea7dbc03cc23d30ec49ff17b675`  
		Last Modified: Tue, 01 Apr 2025 01:09:00 GMT  
		Size: 14.1 MB (14075320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e90c52cdc5fc4ee30f8092a6f287f99307ce44816ddfad47c74cd0186d05a0f`  
		Last Modified: Tue, 01 Apr 2025 01:08:59 GMT  
		Size: 34.2 KB (34250 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:076a9e49e45575312ac51b8dd32b9ea61d58deccae29d75021106b2865250af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228350818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e397fccff1a5dc1d8395e52f9a649bdb8f7ca788d5de1f96837232b22884e016`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 21 Jan 2025 17:21:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c15a7f3f1ea6492a30b69347741d60062b6c3d037ca84ce9221eb389dd33a`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8227bc92840235a12ae22aecf8af32930087b3ccc11feeaa303cd058e9c9d9bf`  
		Last Modified: Tue, 01 Apr 2025 01:10:32 GMT  
		Size: 46.5 MB (46465437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a25639bb1e30f9aee8a00dc1e4da23e6f3bec64ad2e78eed0cb2a0d2377f71c`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570cc21e155e93fb1a6a95a63153ea8d73a7ceb3658d1a083dfa79386cd5c1c`  
		Last Modified: Tue, 01 Apr 2025 01:10:34 GMT  
		Size: 126.8 MB (126797335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475627eb8905295ae6ba215dd3a828b3577326fb7c68fc61514341368947861e`  
		Last Modified: Tue, 01 Apr 2025 01:10:31 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:827b23a80eb6bcfe49863324d1fff08388b99b47cce1fce230d9a40c7e917ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ce636bd86233cc6afc151e6e025413d11d5da185bf7915321ff302be8ce87`

```dockerfile
```

-	Layers:
	-	`sha256:da5d54c11df124ed8c9288d90ba28d50a2ff114fcaf3fe48eb6c5bc75d0ae7d8`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 14.1 MB (14073740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62559d6ca64054841c902099b1aa45c780ac3e84dc35f97f4f4c4bc73faf0a0`  
		Last Modified: Tue, 01 Apr 2025 01:10:30 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:0596fa224cdf3b3355ce3ddbfd7ce77be27ec9e51841dfc5d2e1c8b81eea69d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2b1e754b51504235d37ef7926031d6c0b93c53bff82e49fa1b19b9890541834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241131667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567107cb6971c25f0921ff3c2fa6b460ef636d50ca1365d987cee6bdcce3fd53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cea172a6e83bc32bca4a624b0b5ce27613c2629414100ac0a7cc687f50806a7e`  
		Last Modified: Tue, 01 Apr 2025 00:46:16 GMT  
		Size: 49.1 MB (49091210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac2c594bddf52061dc7bf53aff917472b20932f52a2a899ce0322b2af4da6d`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8acbf2440ce04de0ea33fa37d3077f2b4238414d5908d016a586b35e2109f5`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae51f7de1fbaced1d16dfd4204950dca0e01ecb2d8a95ba40e8dad897718d01`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 6.9 MB (6896405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ead3e96e6b8851ecf2ad0368f7fd7e0f2ef7dc5d2853ee59ddb53f743133c7`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c3ac51f88784e2b57b41de9749e0f05c1a8558cef8cdb8d34e3c6a69b3e5f`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f239a40e6224e119bcf17d0f627a4e978a31a33e5c9d9e89ba15b65f3903b0`  
		Last Modified: Tue, 01 Apr 2025 01:09:14 GMT  
		Size: 48.4 MB (48417200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11056354384f935145933fe4e15a812030cc6e2454b41a0a3eae1d1ff6cdf55`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49978e7ccddf9237ceb5f84b79d4a16368e58b5be1af59807dcab53836be55b1`  
		Last Modified: Tue, 01 Apr 2025 01:09:17 GMT  
		Size: 135.7 MB (135734364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548990e33276fd1718e31016eea5952f8a76b5fad1d12d229992dfb66e1f95bb`  
		Last Modified: Tue, 01 Apr 2025 01:09:13 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:b50a02900983951337f39297a39251f7df41bbf4a04108dea0f38950b44bc61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14120925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6685e15c5d271c74fe6e2a2602386eae48559f9cca5e2a323c38a8e89c95fd`

```dockerfile
```

-	Layers:
	-	`sha256:1356c3df5d8faaceddd953217bc8972c7394106dbf88031ee57257d0fcb55cc2`  
		Last Modified: Tue, 01 Apr 2025 01:09:12 GMT  
		Size: 14.1 MB (14085607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f916cb69f0c853c848086d7e1cb4a10c8f80fa8f2d1f643fd612bbbcc1d63624`  
		Last Modified: Tue, 01 Apr 2025 01:09:11 GMT  
		Size: 35.3 KB (35318 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:4473b639b94f6fda73cef56c184947a2f24379febfb9eab6111b28e5d135b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236518173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2700d94f59a83555cf99a55a364048d584f0c87dd3bc5f919b52bf571b24a04a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 22 Jan 2025 17:15:22 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_MAJOR=innovation
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENV MYSQL_SHELL_VERSION=9.2.0-1.el9
# Wed, 22 Jan 2025 17:15:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 22 Jan 2025 17:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 17:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 17:15:22 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 22 Jan 2025 17:15:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fa07288abb8be04834f9e99f40dceaefb14fa41d27fa9683a1d524c14e62d02b`  
		Last Modified: Tue, 01 Apr 2025 00:16:10 GMT  
		Size: 47.7 MB (47674823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d246ada2dc1c8dff788f71c273894dc66a009dd3ead32103c917c92433ae3`  
		Last Modified: Tue, 01 Apr 2025 01:08:46 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403da7fd01e2a1849d0f21ab24eac8be7d638730fb8af6c3e7cbf6d1f44cc304`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d86ac38d695a731745e6b145ae7bc730a2db97eac8288eedecb0367457a9b`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 6.5 MB (6490300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df6f366614fc634cf140722209bca9f4a0652e91158324c3521634475ba054`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19736db5e51745bf47f1681e109560595a55918525835d1d5c366c219067dbe4`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272f6449e9f1e0cb14137432f92d5916d5bf120469543dfd2c19437d2ad2fd98`  
		Last Modified: Tue, 01 Apr 2025 01:08:50 GMT  
		Size: 47.3 MB (47296009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddc2126e5fd9ad00bd16674c2becadd7acd9853f640d9ab4fc68ac56307d23b`  
		Last Modified: Tue, 01 Apr 2025 01:08:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa861cc3c4c4fe69d64b19f65c57730cf651013969fd6afdca8e5ce76212ef4a`  
		Last Modified: Tue, 01 Apr 2025 01:08:52 GMT  
		Size: 134.1 MB (134134109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735441d7e64a1db6fc77318144d59bfc4a6518ca5389219085151ca69013933a`  
		Last Modified: Tue, 01 Apr 2025 01:08:49 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7707da69925d48c5fab08a7c7b2a5f4a1c6f33ab203d094be60ec2c8a245bd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14119722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d657bc85b3d6d3c6ca7a0c6a91b3517aa0cf1ec90d3bf314f9e5f67bfe0721`

```dockerfile
```

-	Layers:
	-	`sha256:7aa41a10efec3986e6f96669e17dc48c933980c204e18c4a7dfc6a18a4580c16`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 14.1 MB (14084063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c479a9f66e80424e21a550ad43c305676a12cee5459f6f4c5d3ab333d5fba342`  
		Last Modified: Tue, 01 Apr 2025 01:08:47 GMT  
		Size: 35.7 KB (35659 bytes)  
		MIME: application/vnd.in-toto+json
