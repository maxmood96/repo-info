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
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:64756cc92f707eb504496d774353990bcb0f6999ddf598b6ad188f2da66bd000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:ce4d5c5f9df534fb059e6826805ad7dc3cb431589d4d99cc0869f5ee766e0f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123df39bc7c56bb6e40f8e5ef90469cc191dd7afcbf6e0d618c61a12e225dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:06 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:13:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6375ec02106fda1bca765991c2ae7e94feee38406b82fe4a75ba218117352f73`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771773a1fe7a287a99961aa418480b426afac3fd952ff665679460a025bfb081`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 783.5 KB (783540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b8cfb10b4105aba2598ceaf2ff12fa912a9b79019f490d6012cf5a26a72150`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378718ee973de3d06994e102aae9f8bc8502d19fc445a2fd10aad5072f3e41f`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5915b0e5580c575ffc903550eb7154ed40c8061183b4fd7c388b22777a00a763`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c3210ab1f66cb810209d98054f584dac71e7d7400353564836ee757ce4b56f`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 49.9 MB (49918005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440208b3f29f4ead9129c30126fa8d16b9dfed3f9b589c15f1c2d2e1106a0a94`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee8ef3b9fc071e2328d497ccfe791a71384581d555be43b0dc71901ddb1d11`  
		Last Modified: Fri, 20 Mar 2026 01:14:12 GMT  
		Size: 128.1 MB (128099516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8097e7c26be9086d1cee34da0fc4d3830a03f866ecc6c90089bf8e21a99345`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940ecf5daecbcace9f80639c1e40dc1b4390d0dc96b5440bed69d06ad424b52`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:bb4568940fac09636f9ee1f2cd7f98666e1cf3f0734007f7cb1c163fedfd6620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59286c3f0b5161d82256b71b1abc451fe0bbb44c2c23f3c6612f9b76828c5058`

```dockerfile
```

-	Layers:
	-	`sha256:2f1dcce71f1f47fe50eed7e6dd19c46846d2b25e43d4f4ace88b2fbad520a6b0`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0490608ca276baadbf276411a5d1b70bcade3b2b81b1eac3331d022ab0f4e8`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9aa668d29346670d0181fe7ee47126fd66d6599be3ddb3b9b2b51bfb436fe87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227897540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62287ffe3b1ee6e69aa60af0a4661e891adcd5c20489cd1bde504dc905c4e3b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:14:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37801a280bef1fe3325a71cd773bbf854e22a2184c62a10c7d693380ca9208e`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c256042de94f132b31f5afd1bb6ab9498c5a7578ff0ed1ccd331c60881be54f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc36d34517290f4cd9a595baea5ebd7f4396ccb7084f1796351e61a79045218`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.8 MB (5792065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de024cb1a2db8002a8d18591badee6bcfeb30b19f6ee9b6347c92376364779`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5de6158b5fb6b66997ceb49e11ff6eeef7c5ba3f226691f49da496674c56b9`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdcd51b74aa12ff8f31f02e0e546687d40b024ae6ab4e956030a0315280078`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 48.8 MB (48773950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8c26676ac8e5ada80cf9c9446acaafc80f7c57c5ab2f90d2889110e35a090`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941fde55339e77f361f98275c960d86fe8c10a1168adcdf0d313fe934d04b58`  
		Last Modified: Fri, 20 Mar 2026 01:14:46 GMT  
		Size: 126.7 MB (126686421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00d06eab7f5f65bcfadb7051024b2701c87e25765f55d2ba97c3dcdeb118a41`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c435c281e974bcd4b051f7635150a2ce143e8aad6efb7749ef6aa8c7ccc0c4`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:9ff5d100885b7ab8eb90834b399c109d35924f44442287e784b91c817ef03fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4052e2ee08ed2bbb318fc6f8245952f3495227ba78bb304d628a85e0ef135e1e`

```dockerfile
```

-	Layers:
	-	`sha256:cb30400a5864a7ceedc073fbc9f5d6c703c434d89bf558fabdd5291fe843d3b6`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adcca81989c4a5716fc5fc00a75a0479151ea002e12370be70408364f3986cc`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:e90eaf1db3a7032d0dd1ea78141014f173eaeba62229a96124228df653e2db96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:9563a2f64eaa2cdc9164de2d2a76ddafce4356a9d6d534aeb8044e5dcd640326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aa3e7f83cc1b63f2697c5bd89c2248b808d9d5373a5d4f3a72dee2d3a61163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:42:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 16 Mar 2026 22:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:42:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Mon, 16 Mar 2026 22:42:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Mar 2026 22:42:53 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 16 Mar 2026 22:42:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68e614f27fbb413a176db837874d771751afcca8680518b8b9502afc5f3f85`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4916b47a0e84df19644fae91a15098b6634fac737a2dc6ff4c4bc10158a51c`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.4 MB (4423383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383ad717a22e9868a341a2c105ec87a1d0aada2aabe3cbddfd05c8b708823a7`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.2 MB (1248711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4c7e0f678dbdd1a352ce271395789d5c64b8f0bca208afb450ace5cbdf366`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc241f96e4f4237388308240a0d3532a480cbfae6db486e06a933d88f37a85`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 15.3 MB (15295787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830c5b026eb8004c0bad07fdee10cee28b6830bf597310870b56ca3b63b2af7`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064364b837bd9a375eea0c15eee508aee14fed141e2c3c47ba9583f319afa26d`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463ceca1d5fa880b50531fcc0da99b699a7e9a471e594667c112ae7fa1a05e9`  
		Last Modified: Mon, 16 Mar 2026 22:43:20 GMT  
		Size: 134.2 MB (134249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ac8f78e4c19796261b22605a397c62e77b481173d0dfc5d07306c58bb23b`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5de9a02a13f92300fb3cf22b4b9a4e16de2e84f81bfb4ecd80088d9ef58c1d`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321c51e8c3ade48a41e496c8f1b13ed64d59cd6a6a1ad38db7609e842822481`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ce17c4970b9a0db908872dbb4dd7fec01974861cacbcff376697fbd01e808e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e37d0628bc4f7ccd8343a70287b871e61b6201d3ee59eb7bbdb348292bb1de`

```dockerfile
```

-	Layers:
	-	`sha256:18b2e975dbe39eeb41189cd49942890d85eb20e7c55f4a0c47340703a5f69d9d`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1686dab13c765d69e9f26a96e606e8b28b93dc64a6a65ad23ff6fd3f221f65bb`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:e90eaf1db3a7032d0dd1ea78141014f173eaeba62229a96124228df653e2db96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:9563a2f64eaa2cdc9164de2d2a76ddafce4356a9d6d534aeb8044e5dcd640326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aa3e7f83cc1b63f2697c5bd89c2248b808d9d5373a5d4f3a72dee2d3a61163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:42:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 16 Mar 2026 22:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:42:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Mon, 16 Mar 2026 22:42:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Mar 2026 22:42:53 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 16 Mar 2026 22:42:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68e614f27fbb413a176db837874d771751afcca8680518b8b9502afc5f3f85`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4916b47a0e84df19644fae91a15098b6634fac737a2dc6ff4c4bc10158a51c`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.4 MB (4423383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383ad717a22e9868a341a2c105ec87a1d0aada2aabe3cbddfd05c8b708823a7`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.2 MB (1248711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4c7e0f678dbdd1a352ce271395789d5c64b8f0bca208afb450ace5cbdf366`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc241f96e4f4237388308240a0d3532a480cbfae6db486e06a933d88f37a85`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 15.3 MB (15295787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830c5b026eb8004c0bad07fdee10cee28b6830bf597310870b56ca3b63b2af7`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064364b837bd9a375eea0c15eee508aee14fed141e2c3c47ba9583f319afa26d`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463ceca1d5fa880b50531fcc0da99b699a7e9a471e594667c112ae7fa1a05e9`  
		Last Modified: Mon, 16 Mar 2026 22:43:20 GMT  
		Size: 134.2 MB (134249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ac8f78e4c19796261b22605a397c62e77b481173d0dfc5d07306c58bb23b`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5de9a02a13f92300fb3cf22b4b9a4e16de2e84f81bfb4ecd80088d9ef58c1d`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321c51e8c3ade48a41e496c8f1b13ed64d59cd6a6a1ad38db7609e842822481`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ce17c4970b9a0db908872dbb4dd7fec01974861cacbcff376697fbd01e808e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e37d0628bc4f7ccd8343a70287b871e61b6201d3ee59eb7bbdb348292bb1de`

```dockerfile
```

-	Layers:
	-	`sha256:18b2e975dbe39eeb41189cd49942890d85eb20e7c55f4a0c47340703a5f69d9d`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1686dab13c765d69e9f26a96e606e8b28b93dc64a6a65ad23ff6fd3f221f65bb`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:64756cc92f707eb504496d774353990bcb0f6999ddf598b6ad188f2da66bd000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ce4d5c5f9df534fb059e6826805ad7dc3cb431589d4d99cc0869f5ee766e0f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123df39bc7c56bb6e40f8e5ef90469cc191dd7afcbf6e0d618c61a12e225dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:06 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:13:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6375ec02106fda1bca765991c2ae7e94feee38406b82fe4a75ba218117352f73`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771773a1fe7a287a99961aa418480b426afac3fd952ff665679460a025bfb081`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 783.5 KB (783540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b8cfb10b4105aba2598ceaf2ff12fa912a9b79019f490d6012cf5a26a72150`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378718ee973de3d06994e102aae9f8bc8502d19fc445a2fd10aad5072f3e41f`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5915b0e5580c575ffc903550eb7154ed40c8061183b4fd7c388b22777a00a763`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c3210ab1f66cb810209d98054f584dac71e7d7400353564836ee757ce4b56f`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 49.9 MB (49918005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440208b3f29f4ead9129c30126fa8d16b9dfed3f9b589c15f1c2d2e1106a0a94`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee8ef3b9fc071e2328d497ccfe791a71384581d555be43b0dc71901ddb1d11`  
		Last Modified: Fri, 20 Mar 2026 01:14:12 GMT  
		Size: 128.1 MB (128099516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8097e7c26be9086d1cee34da0fc4d3830a03f866ecc6c90089bf8e21a99345`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940ecf5daecbcace9f80639c1e40dc1b4390d0dc96b5440bed69d06ad424b52`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bb4568940fac09636f9ee1f2cd7f98666e1cf3f0734007f7cb1c163fedfd6620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59286c3f0b5161d82256b71b1abc451fe0bbb44c2c23f3c6612f9b76828c5058`

```dockerfile
```

-	Layers:
	-	`sha256:2f1dcce71f1f47fe50eed7e6dd19c46846d2b25e43d4f4ace88b2fbad520a6b0`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0490608ca276baadbf276411a5d1b70bcade3b2b81b1eac3331d022ab0f4e8`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9aa668d29346670d0181fe7ee47126fd66d6599be3ddb3b9b2b51bfb436fe87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227897540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62287ffe3b1ee6e69aa60af0a4661e891adcd5c20489cd1bde504dc905c4e3b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:14:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37801a280bef1fe3325a71cd773bbf854e22a2184c62a10c7d693380ca9208e`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c256042de94f132b31f5afd1bb6ab9498c5a7578ff0ed1ccd331c60881be54f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc36d34517290f4cd9a595baea5ebd7f4396ccb7084f1796351e61a79045218`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.8 MB (5792065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de024cb1a2db8002a8d18591badee6bcfeb30b19f6ee9b6347c92376364779`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5de6158b5fb6b66997ceb49e11ff6eeef7c5ba3f226691f49da496674c56b9`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdcd51b74aa12ff8f31f02e0e546687d40b024ae6ab4e956030a0315280078`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 48.8 MB (48773950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8c26676ac8e5ada80cf9c9446acaafc80f7c57c5ab2f90d2889110e35a090`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941fde55339e77f361f98275c960d86fe8c10a1168adcdf0d313fe934d04b58`  
		Last Modified: Fri, 20 Mar 2026 01:14:46 GMT  
		Size: 126.7 MB (126686421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00d06eab7f5f65bcfadb7051024b2701c87e25765f55d2ba97c3dcdeb118a41`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c435c281e974bcd4b051f7635150a2ce143e8aad6efb7749ef6aa8c7ccc0c4`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9ff5d100885b7ab8eb90834b399c109d35924f44442287e784b91c817ef03fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4052e2ee08ed2bbb318fc6f8245952f3495227ba78bb304d628a85e0ef135e1e`

```dockerfile
```

-	Layers:
	-	`sha256:cb30400a5864a7ceedc073fbc9f5d6c703c434d89bf558fabdd5291fe843d3b6`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adcca81989c4a5716fc5fc00a75a0479151ea002e12370be70408364f3986cc`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:64756cc92f707eb504496d774353990bcb0f6999ddf598b6ad188f2da66bd000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ce4d5c5f9df534fb059e6826805ad7dc3cb431589d4d99cc0869f5ee766e0f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123df39bc7c56bb6e40f8e5ef90469cc191dd7afcbf6e0d618c61a12e225dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:06 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:13:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6375ec02106fda1bca765991c2ae7e94feee38406b82fe4a75ba218117352f73`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771773a1fe7a287a99961aa418480b426afac3fd952ff665679460a025bfb081`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 783.5 KB (783540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b8cfb10b4105aba2598ceaf2ff12fa912a9b79019f490d6012cf5a26a72150`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378718ee973de3d06994e102aae9f8bc8502d19fc445a2fd10aad5072f3e41f`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5915b0e5580c575ffc903550eb7154ed40c8061183b4fd7c388b22777a00a763`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c3210ab1f66cb810209d98054f584dac71e7d7400353564836ee757ce4b56f`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 49.9 MB (49918005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440208b3f29f4ead9129c30126fa8d16b9dfed3f9b589c15f1c2d2e1106a0a94`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee8ef3b9fc071e2328d497ccfe791a71384581d555be43b0dc71901ddb1d11`  
		Last Modified: Fri, 20 Mar 2026 01:14:12 GMT  
		Size: 128.1 MB (128099516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8097e7c26be9086d1cee34da0fc4d3830a03f866ecc6c90089bf8e21a99345`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940ecf5daecbcace9f80639c1e40dc1b4390d0dc96b5440bed69d06ad424b52`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bb4568940fac09636f9ee1f2cd7f98666e1cf3f0734007f7cb1c163fedfd6620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59286c3f0b5161d82256b71b1abc451fe0bbb44c2c23f3c6612f9b76828c5058`

```dockerfile
```

-	Layers:
	-	`sha256:2f1dcce71f1f47fe50eed7e6dd19c46846d2b25e43d4f4ace88b2fbad520a6b0`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0490608ca276baadbf276411a5d1b70bcade3b2b81b1eac3331d022ab0f4e8`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9aa668d29346670d0181fe7ee47126fd66d6599be3ddb3b9b2b51bfb436fe87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227897540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62287ffe3b1ee6e69aa60af0a4661e891adcd5c20489cd1bde504dc905c4e3b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:14:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37801a280bef1fe3325a71cd773bbf854e22a2184c62a10c7d693380ca9208e`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c256042de94f132b31f5afd1bb6ab9498c5a7578ff0ed1ccd331c60881be54f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc36d34517290f4cd9a595baea5ebd7f4396ccb7084f1796351e61a79045218`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.8 MB (5792065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de024cb1a2db8002a8d18591badee6bcfeb30b19f6ee9b6347c92376364779`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5de6158b5fb6b66997ceb49e11ff6eeef7c5ba3f226691f49da496674c56b9`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdcd51b74aa12ff8f31f02e0e546687d40b024ae6ab4e956030a0315280078`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 48.8 MB (48773950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8c26676ac8e5ada80cf9c9446acaafc80f7c57c5ab2f90d2889110e35a090`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941fde55339e77f361f98275c960d86fe8c10a1168adcdf0d313fe934d04b58`  
		Last Modified: Fri, 20 Mar 2026 01:14:46 GMT  
		Size: 126.7 MB (126686421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00d06eab7f5f65bcfadb7051024b2701c87e25765f55d2ba97c3dcdeb118a41`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c435c281e974bcd4b051f7635150a2ce143e8aad6efb7749ef6aa8c7ccc0c4`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9ff5d100885b7ab8eb90834b399c109d35924f44442287e784b91c817ef03fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4052e2ee08ed2bbb318fc6f8245952f3495227ba78bb304d628a85e0ef135e1e`

```dockerfile
```

-	Layers:
	-	`sha256:cb30400a5864a7ceedc073fbc9f5d6c703c434d89bf558fabdd5291fe843d3b6`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adcca81989c4a5716fc5fc00a75a0479151ea002e12370be70408364f3986cc`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:64756cc92f707eb504496d774353990bcb0f6999ddf598b6ad188f2da66bd000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:ce4d5c5f9df534fb059e6826805ad7dc3cb431589d4d99cc0869f5ee766e0f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123df39bc7c56bb6e40f8e5ef90469cc191dd7afcbf6e0d618c61a12e225dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:06 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:13:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6375ec02106fda1bca765991c2ae7e94feee38406b82fe4a75ba218117352f73`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771773a1fe7a287a99961aa418480b426afac3fd952ff665679460a025bfb081`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 783.5 KB (783540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b8cfb10b4105aba2598ceaf2ff12fa912a9b79019f490d6012cf5a26a72150`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378718ee973de3d06994e102aae9f8bc8502d19fc445a2fd10aad5072f3e41f`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5915b0e5580c575ffc903550eb7154ed40c8061183b4fd7c388b22777a00a763`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c3210ab1f66cb810209d98054f584dac71e7d7400353564836ee757ce4b56f`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 49.9 MB (49918005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440208b3f29f4ead9129c30126fa8d16b9dfed3f9b589c15f1c2d2e1106a0a94`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee8ef3b9fc071e2328d497ccfe791a71384581d555be43b0dc71901ddb1d11`  
		Last Modified: Fri, 20 Mar 2026 01:14:12 GMT  
		Size: 128.1 MB (128099516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8097e7c26be9086d1cee34da0fc4d3830a03f866ecc6c90089bf8e21a99345`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940ecf5daecbcace9f80639c1e40dc1b4390d0dc96b5440bed69d06ad424b52`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:bb4568940fac09636f9ee1f2cd7f98666e1cf3f0734007f7cb1c163fedfd6620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59286c3f0b5161d82256b71b1abc451fe0bbb44c2c23f3c6612f9b76828c5058`

```dockerfile
```

-	Layers:
	-	`sha256:2f1dcce71f1f47fe50eed7e6dd19c46846d2b25e43d4f4ace88b2fbad520a6b0`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0490608ca276baadbf276411a5d1b70bcade3b2b81b1eac3331d022ab0f4e8`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9aa668d29346670d0181fe7ee47126fd66d6599be3ddb3b9b2b51bfb436fe87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227897540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62287ffe3b1ee6e69aa60af0a4661e891adcd5c20489cd1bde504dc905c4e3b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:14:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37801a280bef1fe3325a71cd773bbf854e22a2184c62a10c7d693380ca9208e`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c256042de94f132b31f5afd1bb6ab9498c5a7578ff0ed1ccd331c60881be54f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc36d34517290f4cd9a595baea5ebd7f4396ccb7084f1796351e61a79045218`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.8 MB (5792065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de024cb1a2db8002a8d18591badee6bcfeb30b19f6ee9b6347c92376364779`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5de6158b5fb6b66997ceb49e11ff6eeef7c5ba3f226691f49da496674c56b9`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdcd51b74aa12ff8f31f02e0e546687d40b024ae6ab4e956030a0315280078`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 48.8 MB (48773950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8c26676ac8e5ada80cf9c9446acaafc80f7c57c5ab2f90d2889110e35a090`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941fde55339e77f361f98275c960d86fe8c10a1168adcdf0d313fe934d04b58`  
		Last Modified: Fri, 20 Mar 2026 01:14:46 GMT  
		Size: 126.7 MB (126686421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00d06eab7f5f65bcfadb7051024b2701c87e25765f55d2ba97c3dcdeb118a41`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c435c281e974bcd4b051f7635150a2ce143e8aad6efb7749ef6aa8c7ccc0c4`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:9ff5d100885b7ab8eb90834b399c109d35924f44442287e784b91c817ef03fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4052e2ee08ed2bbb318fc6f8245952f3495227ba78bb304d628a85e0ef135e1e`

```dockerfile
```

-	Layers:
	-	`sha256:cb30400a5864a7ceedc073fbc9f5d6c703c434d89bf558fabdd5291fe843d3b6`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adcca81989c4a5716fc5fc00a75a0479151ea002e12370be70408364f3986cc`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:e90eaf1db3a7032d0dd1ea78141014f173eaeba62229a96124228df653e2db96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:9563a2f64eaa2cdc9164de2d2a76ddafce4356a9d6d534aeb8044e5dcd640326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aa3e7f83cc1b63f2697c5bd89c2248b808d9d5373a5d4f3a72dee2d3a61163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:42:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 16 Mar 2026 22:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:42:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Mon, 16 Mar 2026 22:42:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Mar 2026 22:42:53 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 16 Mar 2026 22:42:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68e614f27fbb413a176db837874d771751afcca8680518b8b9502afc5f3f85`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4916b47a0e84df19644fae91a15098b6634fac737a2dc6ff4c4bc10158a51c`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.4 MB (4423383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383ad717a22e9868a341a2c105ec87a1d0aada2aabe3cbddfd05c8b708823a7`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.2 MB (1248711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4c7e0f678dbdd1a352ce271395789d5c64b8f0bca208afb450ace5cbdf366`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc241f96e4f4237388308240a0d3532a480cbfae6db486e06a933d88f37a85`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 15.3 MB (15295787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830c5b026eb8004c0bad07fdee10cee28b6830bf597310870b56ca3b63b2af7`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064364b837bd9a375eea0c15eee508aee14fed141e2c3c47ba9583f319afa26d`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463ceca1d5fa880b50531fcc0da99b699a7e9a471e594667c112ae7fa1a05e9`  
		Last Modified: Mon, 16 Mar 2026 22:43:20 GMT  
		Size: 134.2 MB (134249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ac8f78e4c19796261b22605a397c62e77b481173d0dfc5d07306c58bb23b`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5de9a02a13f92300fb3cf22b4b9a4e16de2e84f81bfb4ecd80088d9ef58c1d`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321c51e8c3ade48a41e496c8f1b13ed64d59cd6a6a1ad38db7609e842822481`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ce17c4970b9a0db908872dbb4dd7fec01974861cacbcff376697fbd01e808e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e37d0628bc4f7ccd8343a70287b871e61b6201d3ee59eb7bbdb348292bb1de`

```dockerfile
```

-	Layers:
	-	`sha256:18b2e975dbe39eeb41189cd49942890d85eb20e7c55f4a0c47340703a5f69d9d`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1686dab13c765d69e9f26a96e606e8b28b93dc64a6a65ad23ff6fd3f221f65bb`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:e90eaf1db3a7032d0dd1ea78141014f173eaeba62229a96124228df653e2db96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:9563a2f64eaa2cdc9164de2d2a76ddafce4356a9d6d534aeb8044e5dcd640326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aa3e7f83cc1b63f2697c5bd89c2248b808d9d5373a5d4f3a72dee2d3a61163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:42:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 16 Mar 2026 22:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:42:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Mon, 16 Mar 2026 22:42:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Mar 2026 22:42:53 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 16 Mar 2026 22:42:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68e614f27fbb413a176db837874d771751afcca8680518b8b9502afc5f3f85`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4916b47a0e84df19644fae91a15098b6634fac737a2dc6ff4c4bc10158a51c`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.4 MB (4423383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383ad717a22e9868a341a2c105ec87a1d0aada2aabe3cbddfd05c8b708823a7`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.2 MB (1248711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4c7e0f678dbdd1a352ce271395789d5c64b8f0bca208afb450ace5cbdf366`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc241f96e4f4237388308240a0d3532a480cbfae6db486e06a933d88f37a85`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 15.3 MB (15295787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830c5b026eb8004c0bad07fdee10cee28b6830bf597310870b56ca3b63b2af7`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064364b837bd9a375eea0c15eee508aee14fed141e2c3c47ba9583f319afa26d`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463ceca1d5fa880b50531fcc0da99b699a7e9a471e594667c112ae7fa1a05e9`  
		Last Modified: Mon, 16 Mar 2026 22:43:20 GMT  
		Size: 134.2 MB (134249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ac8f78e4c19796261b22605a397c62e77b481173d0dfc5d07306c58bb23b`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5de9a02a13f92300fb3cf22b4b9a4e16de2e84f81bfb4ecd80088d9ef58c1d`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321c51e8c3ade48a41e496c8f1b13ed64d59cd6a6a1ad38db7609e842822481`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ce17c4970b9a0db908872dbb4dd7fec01974861cacbcff376697fbd01e808e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e37d0628bc4f7ccd8343a70287b871e61b6201d3ee59eb7bbdb348292bb1de`

```dockerfile
```

-	Layers:
	-	`sha256:18b2e975dbe39eeb41189cd49942890d85eb20e7c55f4a0c47340703a5f69d9d`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1686dab13c765d69e9f26a96e606e8b28b93dc64a6a65ad23ff6fd3f221f65bb`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:64756cc92f707eb504496d774353990bcb0f6999ddf598b6ad188f2da66bd000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ce4d5c5f9df534fb059e6826805ad7dc3cb431589d4d99cc0869f5ee766e0f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123df39bc7c56bb6e40f8e5ef90469cc191dd7afcbf6e0d618c61a12e225dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:06 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:13:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6375ec02106fda1bca765991c2ae7e94feee38406b82fe4a75ba218117352f73`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771773a1fe7a287a99961aa418480b426afac3fd952ff665679460a025bfb081`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 783.5 KB (783540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b8cfb10b4105aba2598ceaf2ff12fa912a9b79019f490d6012cf5a26a72150`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378718ee973de3d06994e102aae9f8bc8502d19fc445a2fd10aad5072f3e41f`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5915b0e5580c575ffc903550eb7154ed40c8061183b4fd7c388b22777a00a763`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c3210ab1f66cb810209d98054f584dac71e7d7400353564836ee757ce4b56f`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 49.9 MB (49918005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440208b3f29f4ead9129c30126fa8d16b9dfed3f9b589c15f1c2d2e1106a0a94`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee8ef3b9fc071e2328d497ccfe791a71384581d555be43b0dc71901ddb1d11`  
		Last Modified: Fri, 20 Mar 2026 01:14:12 GMT  
		Size: 128.1 MB (128099516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8097e7c26be9086d1cee34da0fc4d3830a03f866ecc6c90089bf8e21a99345`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940ecf5daecbcace9f80639c1e40dc1b4390d0dc96b5440bed69d06ad424b52`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bb4568940fac09636f9ee1f2cd7f98666e1cf3f0734007f7cb1c163fedfd6620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59286c3f0b5161d82256b71b1abc451fe0bbb44c2c23f3c6612f9b76828c5058`

```dockerfile
```

-	Layers:
	-	`sha256:2f1dcce71f1f47fe50eed7e6dd19c46846d2b25e43d4f4ace88b2fbad520a6b0`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0490608ca276baadbf276411a5d1b70bcade3b2b81b1eac3331d022ab0f4e8`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9aa668d29346670d0181fe7ee47126fd66d6599be3ddb3b9b2b51bfb436fe87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227897540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62287ffe3b1ee6e69aa60af0a4661e891adcd5c20489cd1bde504dc905c4e3b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:14:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37801a280bef1fe3325a71cd773bbf854e22a2184c62a10c7d693380ca9208e`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c256042de94f132b31f5afd1bb6ab9498c5a7578ff0ed1ccd331c60881be54f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc36d34517290f4cd9a595baea5ebd7f4396ccb7084f1796351e61a79045218`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.8 MB (5792065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de024cb1a2db8002a8d18591badee6bcfeb30b19f6ee9b6347c92376364779`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5de6158b5fb6b66997ceb49e11ff6eeef7c5ba3f226691f49da496674c56b9`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdcd51b74aa12ff8f31f02e0e546687d40b024ae6ab4e956030a0315280078`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 48.8 MB (48773950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8c26676ac8e5ada80cf9c9446acaafc80f7c57c5ab2f90d2889110e35a090`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941fde55339e77f361f98275c960d86fe8c10a1168adcdf0d313fe934d04b58`  
		Last Modified: Fri, 20 Mar 2026 01:14:46 GMT  
		Size: 126.7 MB (126686421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00d06eab7f5f65bcfadb7051024b2701c87e25765f55d2ba97c3dcdeb118a41`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c435c281e974bcd4b051f7635150a2ce143e8aad6efb7749ef6aa8c7ccc0c4`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9ff5d100885b7ab8eb90834b399c109d35924f44442287e784b91c817ef03fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4052e2ee08ed2bbb318fc6f8245952f3495227ba78bb304d628a85e0ef135e1e`

```dockerfile
```

-	Layers:
	-	`sha256:cb30400a5864a7ceedc073fbc9f5d6c703c434d89bf558fabdd5291fe843d3b6`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adcca81989c4a5716fc5fc00a75a0479151ea002e12370be70408364f3986cc`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:64756cc92f707eb504496d774353990bcb0f6999ddf598b6ad188f2da66bd000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ce4d5c5f9df534fb059e6826805ad7dc3cb431589d4d99cc0869f5ee766e0f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232290920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123df39bc7c56bb6e40f8e5ef90469cc191dd7afcbf6e0d618c61a12e225dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:06 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:33 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:13:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6375ec02106fda1bca765991c2ae7e94feee38406b82fe4a75ba218117352f73`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771773a1fe7a287a99961aa418480b426afac3fd952ff665679460a025bfb081`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 783.5 KB (783540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b8cfb10b4105aba2598ceaf2ff12fa912a9b79019f490d6012cf5a26a72150`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378718ee973de3d06994e102aae9f8bc8502d19fc445a2fd10aad5072f3e41f`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5915b0e5580c575ffc903550eb7154ed40c8061183b4fd7c388b22777a00a763`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c3210ab1f66cb810209d98054f584dac71e7d7400353564836ee757ce4b56f`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 49.9 MB (49918005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440208b3f29f4ead9129c30126fa8d16b9dfed3f9b589c15f1c2d2e1106a0a94`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee8ef3b9fc071e2328d497ccfe791a71384581d555be43b0dc71901ddb1d11`  
		Last Modified: Fri, 20 Mar 2026 01:14:12 GMT  
		Size: 128.1 MB (128099516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8097e7c26be9086d1cee34da0fc4d3830a03f866ecc6c90089bf8e21a99345`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940ecf5daecbcace9f80639c1e40dc1b4390d0dc96b5440bed69d06ad424b52`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bb4568940fac09636f9ee1f2cd7f98666e1cf3f0734007f7cb1c163fedfd6620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59286c3f0b5161d82256b71b1abc451fe0bbb44c2c23f3c6612f9b76828c5058`

```dockerfile
```

-	Layers:
	-	`sha256:2f1dcce71f1f47fe50eed7e6dd19c46846d2b25e43d4f4ace88b2fbad520a6b0`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0490608ca276baadbf276411a5d1b70bcade3b2b81b1eac3331d022ab0f4e8`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9aa668d29346670d0181fe7ee47126fd66d6599be3ddb3b9b2b51bfb436fe87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227897540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62287ffe3b1ee6e69aa60af0a4661e891adcd5c20489cd1bde504dc905c4e3b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 20 Mar 2026 01:12:59 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:12:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 20 Mar 2026 01:14:09 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 20 Mar 2026 01:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:09 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37801a280bef1fe3325a71cd773bbf854e22a2184c62a10c7d693380ca9208e`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c256042de94f132b31f5afd1bb6ab9498c5a7578ff0ed1ccd331c60881be54f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 737.5 KB (737527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc36d34517290f4cd9a595baea5ebd7f4396ccb7084f1796351e61a79045218`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.8 MB (5792065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de024cb1a2db8002a8d18591badee6bcfeb30b19f6ee9b6347c92376364779`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5de6158b5fb6b66997ceb49e11ff6eeef7c5ba3f226691f49da496674c56b9`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcdcd51b74aa12ff8f31f02e0e546687d40b024ae6ab4e956030a0315280078`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 48.8 MB (48773950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8c26676ac8e5ada80cf9c9446acaafc80f7c57c5ab2f90d2889110e35a090`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c941fde55339e77f361f98275c960d86fe8c10a1168adcdf0d313fe934d04b58`  
		Last Modified: Fri, 20 Mar 2026 01:14:46 GMT  
		Size: 126.7 MB (126686421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00d06eab7f5f65bcfadb7051024b2701c87e25765f55d2ba97c3dcdeb118a41`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c435c281e974bcd4b051f7635150a2ce143e8aad6efb7749ef6aa8c7ccc0c4`  
		Last Modified: Fri, 20 Mar 2026 01:14:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9ff5d100885b7ab8eb90834b399c109d35924f44442287e784b91c817ef03fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4052e2ee08ed2bbb318fc6f8245952f3495227ba78bb304d628a85e0ef135e1e`

```dockerfile
```

-	Layers:
	-	`sha256:cb30400a5864a7ceedc073fbc9f5d6c703c434d89bf558fabdd5291fe843d3b6`  
		Last Modified: Fri, 20 Mar 2026 01:14:41 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adcca81989c4a5716fc5fc00a75a0479151ea002e12370be70408364f3986cc`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:da906917ca4ace3ba55538b7c2ee97a9bc865ef14a4b6920b021f0249d603f3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:77e7fd3d377ad2d9e7983d457b71ff8a04c0f19e41948d722f15c508a48dcce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233216898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0320de35118bb355866609d2895c07d8d1696e0aa373c5a9a4a4525c99c3224d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:33 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:34 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:34 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:03 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:13:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd28adefbd9efa5e6271ef815f21edb388c28f4d58a002763a747c6861d9f5e`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43105b2d4e4aabb65c7d8d83298d15e18a040ed49946d502faff6a2106673a46`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d4892b7d221ade0bc214e4b02713fce341fef039d27cbf4f01db7aab8f389`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 6.2 MB (6170052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8eed90d752f2cd81cc08291649b38dab6f64f8bad99d489f53c809f519109`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68420c358694c9cbe66f5d9fdd71c848e17daf6cfbb4e62eb534525c5b0b9eec`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50200b0c89a318ccd4b63a6de68d6c8ac57f97e7efbde2e76ae91a8511970cce`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 47.8 MB (47809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ae82fc56341576543092b248c5a702b17b94a24fbb42425bfccde2bad453`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14d7bf02a43e137314cd77f10b9b06fb70f0252d22c2e715dc8970f0033a3d`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 131.1 MB (131133726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c98008674391656bcf0ce9197fb64d4bd735d061129dd3673fe9df342e22e2`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:78b9c0ccea3f476fe11134b1580b7791f1e524879fc212b089beab5885b225b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230b15078b04cfa6a7b86db8b88cd8377e791fac2918c05db7c44307061aaab9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad5e3bd9c41b80a8960c7ab3d4c91a3f39f65d68658c37536f06eb4b1d0ce46`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ed159fbec4ce356112bd9a414ba41c1edf48d5dcf437be9d7f8c22387855dc`  
		Last Modified: Fri, 20 Mar 2026 01:14:06 GMT  
		Size: 34.2 KB (34207 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cccee62518a4bdfa62e8027772cd4be1669033c9af51242d0ad37c252e1e2a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228687218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160a33a7a1db6dd1215c69d3988472742b3fe721ad770cc39f106fe6f22ce3be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 20 Mar 2026 01:12:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:26 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 20 Mar 2026 01:14:06 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:06 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97fa67bd1eebd1fb8aaf306af71080e23815afca19ab74a815bc4e7ea33434`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab19387bfb86ccb52d8dae7f95a381878e7e5bd6ea861807eb9b0ae589a4c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 5.8 MB (5792125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd76274bde54026b44246131a55ddf3e0375f2be61037c52ba8d75b48e7e0`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8424ffc0c72ef42277b6c88cea9b573469d278f7ce8857f0450e59414860d`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a26469b2848717836d235f12bef3253c9b7cc42fbf3518aeb35e8db279991d`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 46.7 MB (46699135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35094554b451d41d323c259cd01d2db6f65d23bb646237b1ea46c932036cc83a`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866893aeb7678007be34659f6fc3a674b1aad1cbf8feee3cb88fb51297d0e0c9`  
		Last Modified: Fri, 20 Mar 2026 01:14:42 GMT  
		Size: 129.6 MB (129550969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143da8c248a8de5107708034aa918673cadbf16979123a6f9a051d727e9001f`  
		Last Modified: Fri, 20 Mar 2026 01:14:40 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:0a64c80220c4479b48b1d36d070c455acf65c318813d6cd1e2c7f969c84fc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5e452e7cf9f128a31464cacf5f831db57cd1f78ba9b3368af0dd6edc0de886`

```dockerfile
```

-	Layers:
	-	`sha256:4ef64a952e35635ea176f51d061c6dfa94d1827486c89e7797583dee73eff277`  
		Last Modified: Fri, 20 Mar 2026 01:14:38 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fac969428a394a4a22ee67ea31095c45f3b137f4f832e440036628ff9bb7d8`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:24e450bbd24f621c71b10404c946cc9ea1cbb0e6e7464b2be2de5193dcf1d05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d1e3f7334b4f647e4e659554d4d8af11ffa1aa8cebd6decbcf1eba33aa2f3f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266354886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ecd26c734662caa005f5b33c3040cbd875351006fae7b15f21573e6b2fef27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:28 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:29 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:12:57 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:13:36 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:13:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:13:36 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:13:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef200aee2ac837f9af036a093258dc647b3a77ccdd0258408c939169c9215e6`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3bc5fe20306056d865a675a00f8e8c28a2132f83fcb5aa53f457786349a96a`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 783.6 KB (783551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83832a620875e5767735eafd995e30bd38c4068d7d076538cfd68ee322f321`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 6.2 MB (6170037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eb4be426a1e5aaf3a55d28d75891f84564e69487a31fdfec83198feb385a87`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38d99426c52e161ae16de965b46d2ed65632a41e3867f7734cd0cdcd3a8548`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b6f683cbda72619818d3c1ba0e9c97f3f4693e933dc605ebaba2ea91f0003`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 51.5 MB (51450674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3633ebbb733a5fd46b7b8e1d3b70f79dcba7b9e1c0bc05a2fb31ae9adc870e`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ae5ec7f3c2e6878df04718147a917111e9b65ab20332eec2fb80513e5ec06`  
		Last Modified: Fri, 20 Mar 2026 01:14:14 GMT  
		Size: 160.6 MB (160630871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee12630a0f387373b78a8aa73973a5c7c64072a6a12946e7d899b548557e`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f58463ee35b126f65583a88a17e2d4d91020a78450565c68a5e9df6046d03aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779063833a854c95bebb95ca0c7ea063b30f93c9e24538ad6e86f919e3a6ab86`

```dockerfile
```

-	Layers:
	-	`sha256:697c144a0375095a3c66cfda792df78c54c6de3de28d5430d3bc9ed28f876238`  
		Last Modified: Fri, 20 Mar 2026 01:14:08 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f88ec2712b718bb339e508230f275a82ed349933e4b20752943a65ba2076f0`  
		Last Modified: Fri, 20 Mar 2026 01:14:07 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6312654adbf6c7fc95739b1646bc6c27addd09f946ecb92374cf4e09bc48a617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261460583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb25041c30c56f51acabb099e27d18272ea2e7904087f2baeed0af611908610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 20 Mar 2026 01:12:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 20 Mar 2026 01:12:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Mar 2026 01:12:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 20 Mar 2026 01:12:56 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 20 Mar 2026 01:13:30 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 20 Mar 2026 01:13:31 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 20 Mar 2026 01:14:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
VOLUME [/var/lib/mysql]
# Fri, 20 Mar 2026 01:14:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 01:14:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 01:14:17 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 20 Mar 2026 01:14:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd468e076f5f72f9287f17234760ca3c0a4343a107dff8555555147620f83658`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6742f724b8597e0ed0f0ea7dcb7251418f72895f7627d883de8feab54ab92c0f`  
		Last Modified: Fri, 20 Mar 2026 01:14:37 GMT  
		Size: 737.5 KB (737530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9ef92a2af442de07e94274e799e4b10cfae5d49761cbb13f1a7cf633cc557`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 5.8 MB (5792134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3544b01d14fe4400a6d45fe84aade219abbaeb3be18d81c680c2aafc8be066`  
		Last Modified: Fri, 20 Mar 2026 01:14:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79027f52ee894bb4918888aeae46a4962bbf2fbabbb3d033e4379880f10e44`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512322a9b1101d2f1404b58f7ca8f09343ef4288a75d7051cf1b14e33cdc3c5`  
		Last Modified: Fri, 20 Mar 2026 01:14:56 GMT  
		Size: 50.1 MB (50085487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ee06ae1885254ef09d5bff76e2956c62dfea46d2194d55f3cbded294dc6a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a795b6ed29054e922369bda5ddc893d56f70fab7a7732b174b12238ce668e69`  
		Last Modified: Fri, 20 Mar 2026 01:14:58 GMT  
		Size: 158.9 MB (158937958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafc12891f62580955d7555e24ab88089f0775a2314ab46f87547b46fd28e86`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:327391d8d6a79eac5b1e211f08c442925fdcba3984316c86137888752e7290e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40910e38767e54d0af6c69606f2d1de3adba9918035776ef987911461e644ee2`

```dockerfile
```

-	Layers:
	-	`sha256:714d9b174b27412795703f838bd591ecc5286ae270f2256712447925954bbd6a`  
		Last Modified: Fri, 20 Mar 2026 01:14:55 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b502d61e919454200e1496fe341f5eb3d8093d6ac1d5c627c692fabeaaa94c6`  
		Last Modified: Fri, 20 Mar 2026 01:14:53 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
